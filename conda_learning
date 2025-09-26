conda 是一个流行的包管理和环境管理工具，广泛用于 Python 及其他编程语言的环境配置。以下是常用的 conda 操作命令，按功能分类整理：


### **一、环境管理**
#### 1. 查看所有环境
```bash
conda env list  # 或 conda info --envs
```
显示当前系统中所有的 conda 环境，当前激活的环境会用 `*` 标记。


#### 2. 创建新环境
```bash
conda create --name <环境名>  # 基础创建（默认Python版本）
conda create --name <环境名> python=3.9  # 指定Python版本
conda create --name <环境名> python=3.9 <包名1> <包名2>  # 创建时同时安装包
```
示例：创建一个名为 `ml_env`、Python 版本为 3.8 的环境，并安装 `numpy`：  
`conda create --name ml_env python=3.8 numpy`


#### 3. 激活环境
```bash
# Windows（CMD/PowerShell）
conda activate <环境名>

# Linux/macOS（终端）
source activate <环境名>  # 旧版本conda
conda activate <环境名>   # 新版本conda（推荐）
```
激活后，终端提示符会显示当前环境名（如 `(ml_env)`）。


#### 4. 退出当前环境
```bash
conda deactivate
```


#### 5. 复制环境
```bash
conda create --name <新环境名> --clone <被复制的环境名>
```


#### 6. 删除环境
```bash
conda remove --name <环境名> --all
```


#### 7. 导出/导入环境配置
- **导出环境到文件**（常用于分享环境依赖）：  
  ```bash
  conda env export --name <环境名> > environment.yml
  ```
  会生成一个 `environment.yml` 文件，包含环境的所有依赖信息。

- **从文件导入环境**：  
  ```bash
  conda env create --file environment.yml
  ```
  会根据 `environment.yml` 中的配置创建新环境。


### **二、包管理**
#### 1. 安装包
```bash
conda install <包名>  # 在当前环境安装包
conda install <包名>=1.2.3  # 安装指定版本
conda install -n <环境名> <包名>  # 在指定环境安装包（无需激活环境）
conda install -c <渠道名> <包名>  # 从指定渠道安装（如conda-forge）
```
示例：从 `conda-forge` 渠道安装 `pandas` 1.5.0 版本：  
`conda install -c conda-forge pandas=1.5.0`


#### 2. 查看当前环境已安装的包
```bash
conda list  # 查看当前环境所有包
conda list <包名>  # 查看指定包是否安装及版本
conda list -n <环境名>  # 查看指定环境的包
```


#### 3. 更新包
```bash
conda update <包名>  # 更新当前环境的指定包
conda update --all  # 更新当前环境的所有包
conda update -n <环境名> <包名>  # 更新指定环境的包
```


#### 4. 卸载包
```bash
conda remove <包名>  # 卸载当前环境的包
conda remove -n <环境名> <包名>  # 卸载指定环境的包
```


### **三、conda 自身管理**
#### 1. 查看 conda 版本
```bash
conda --version  # 或 conda -V
```


#### 2. 更新 conda
```bash
conda update conda  # 更新conda本身
conda update anaconda  # 如果安装了Anaconda，更新Anaconda发行版
```


#### 3. 清理缓存（释放磁盘空间）
```bash
conda clean --all  # 清理所有缓存（包括未使用的包、tarballs等）
conda clean --packages  # 仅清理未使用的包
```


### **四、其他常用命令**
- 搜索包（查看可用版本和渠道）：  
  ```bash
  conda search <包名>
  ```

- 查看 conda 配置（如默认渠道）：  
  ```bash
  conda config --show
  ```

- 添加镜像渠道（加速下载，如国内镜像）：  
  ```bash
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  conda config --set show_channel_urls yes  # 显示包的安装渠道
  ```
