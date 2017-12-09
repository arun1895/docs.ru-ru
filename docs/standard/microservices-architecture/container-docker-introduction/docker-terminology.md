---
title: "Терминология docker"
description: "Архитектура Микрослужбами .NET для приложений .NET в контейнерах | Терминология docker"
keywords: "Docker, микрослужбы, ASP.NET, контейнер"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 885b1fbd3369dec54ebde21a5378630c764f852d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="docker-terminology"></a><span data-ttu-id="30de2-104">Терминология docker</span><span class="sxs-lookup"><span data-stu-id="30de2-104">Docker terminology</span></span>

<span data-ttu-id="30de2-105">В этом разделе перечислены термины и определения, следует ознакомиться с прежде чем клиент получит глубоко в Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-105">This section lists terms and definitions you should be familiar with before getting deeper into Docker.</span></span> <span data-ttu-id="30de2-106">Определения см. в разделе подробную [Глоссарий](https://docs.docker.com/v1.11/engine/reference/glossary/) предоставляемые Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-106">For further definitions, see the extensive [glossary](https://docs.docker.com/v1.11/engine/reference/glossary/) provided by Docker .</span></span>

<span data-ttu-id="30de2-107">**Образ контейнера**: пакет с зависимостями и сведения, необходимые для создания контейнера.</span><span class="sxs-lookup"><span data-stu-id="30de2-107">**Container image**: A package with all the dependencies and information needed to create a container.</span></span> <span data-ttu-id="30de2-108">Изображение включает все зависимости (например, frameworks) плюс конфигурации развертывания и выполнения для использования средой выполнения контейнера.</span><span class="sxs-lookup"><span data-stu-id="30de2-108">An image includes all the dependencies (such as frameworks) plus deployment and execution configuration to be used by a container runtime.</span></span> <span data-ttu-id="30de2-109">Как правило изображение является производным от нескольких базовые образы, которые являются слои нижестоящей друг с другом, образуя контейнера файловой системы.</span><span class="sxs-lookup"><span data-stu-id="30de2-109">Usually, an image derives from multiple base images that are layers stacked on top of each other to form the container’s filesystem.</span></span> <span data-ttu-id="30de2-110">Изображение является неизменяемым, после его создания.</span><span class="sxs-lookup"><span data-stu-id="30de2-110">An image is immutable once it has been created.</span></span>

<span data-ttu-id="30de2-111">**Контейнер**: экземпляр образа Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-111">**Container**: An instance of a Docker image.</span></span> <span data-ttu-id="30de2-112">Контейнер представляет выполнение одного приложения, процесса или службы.</span><span class="sxs-lookup"><span data-stu-id="30de2-112">A container represents the execution of a single application, process, or service.</span></span> <span data-ttu-id="30de2-113">Он состоит из содержимого образа Docker, среды выполнения и стандартный набор инструкций.</span><span class="sxs-lookup"><span data-stu-id="30de2-113">It consists of the contents of a Docker image, an execution environment, and a standard set of instructions.</span></span> <span data-ttu-id="30de2-114">Масштабирование службы, создается несколько экземпляров контейнера из того же образа.</span><span class="sxs-lookup"><span data-stu-id="30de2-114">When scaling a service, you create multiple instances of a container from the same image.</span></span> <span data-ttu-id="30de2-115">Или пакетного задания можно создать несколько контейнеров из одного образа передачи различных параметров для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30de2-115">Or a batch job can create multiple containers from the same image, passing different parameters to each instance.</span></span>

<span data-ttu-id="30de2-116">**Тег**: знак или метки, можно применить к изображениям, чтобы можно было идентифицировать различные изображения или версии одного образа (в зависимости от номера версии или целевой среды).</span><span class="sxs-lookup"><span data-stu-id="30de2-116">**Tag**: A mark or label you can apply to images so that different images or versions of the same image (depending on the version number or the target environment) can be identified.</span></span>

<span data-ttu-id="30de2-117">**Dockerfile**: текстовый файл, содержащий инструкции для создания образа Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-117">**Dockerfile**: A text file that contains instructions for how to build a Docker image.</span></span>

<span data-ttu-id="30de2-118">**Построение**: действие построения образа контейнера на основе сведений и контекст, предоставляемый его Dockerfile, а также дополнительные файлы в папке, где создан образ.</span><span class="sxs-lookup"><span data-stu-id="30de2-118">**Build**: The action of building a container image based on the information and context provided by its Dockerfile, plus additional files in the folder where the image is built.</span></span> <span data-ttu-id="30de2-119">Можно создавать изображения с помощью команды Docker docker сборки.</span><span class="sxs-lookup"><span data-stu-id="30de2-119">You can build images with the Docker docker build command.</span></span>

<span data-ttu-id="30de2-120">**Репозиторий (репозитория)**: коллекцию связанных образы Docker, помеченные тегом, который указывает версию образа.</span><span class="sxs-lookup"><span data-stu-id="30de2-120">**Repository (repo)**: A collection of related Docker images, labeled with a tag that indicates the image version.</span></span> <span data-ttu-id="30de2-121">Некоторые репозиториев содержат несколько вариантов конкретный образ, например изображение, содержащий изображение, содержащее только среды выполнения (светлее) (более сложной), пакеты SDK, и т. д. Эти варианты можно пометить тегами.</span><span class="sxs-lookup"><span data-stu-id="30de2-121">Some repos contain multiple variants of a specific image, such as an image containing SDKs (heavier), an image containing only runtimes (lighter), etc. Those variants can be marked with tags.</span></span> <span data-ttu-id="30de2-122">Один репозиторий может содержать вариантов платформы, например в Linux образ и образ Windows.</span><span class="sxs-lookup"><span data-stu-id="30de2-122">A single repo can contain platform variants, such as a Linux image and a Windows image.</span></span>

<span data-ttu-id="30de2-123">**Реестр**: служба, предоставляющая доступ к репозиторию.</span><span class="sxs-lookup"><span data-stu-id="30de2-123">**Registry**: A service that provides access to repositories.</span></span> <span data-ttu-id="30de2-124">В реестре по умолчанию для большинства общедоступных изображений [Docker Hub](https://hub.docker.com/) (владеют Docker для организации).</span><span class="sxs-lookup"><span data-stu-id="30de2-124">The default registry for most public images is [Docker Hub](https://hub.docker.com/) (owned by Docker as an organization).</span></span> <span data-ttu-id="30de2-125">Реестра обычно содержит репозиториев из нескольких команд.</span><span class="sxs-lookup"><span data-stu-id="30de2-125">A registry usually contains repositories from multiple teams.</span></span> <span data-ttu-id="30de2-126">Компании используют частных реестрах для хранения и управления изображения, которые они создали.</span><span class="sxs-lookup"><span data-stu-id="30de2-126">Companies often have private registries to store and manage images they’ve created.</span></span> <span data-ttu-id="30de2-127">Azure реестра контейнера еще один пример.</span><span class="sxs-lookup"><span data-stu-id="30de2-127">Azure Container Registry is another example.</span></span>

<span data-ttu-id="30de2-128">**Docker Hub**: открытого реестра для отправки изображений и работать с ними.</span><span class="sxs-lookup"><span data-stu-id="30de2-128">**Docker Hub**: A public registry to upload images and work with them.</span></span> <span data-ttu-id="30de2-129">Docker Hub предоставляет Docker размещения изображения, открытые или закрытые реестров, триггеров и обработчики web и интеграцию с GitHub и Bitbucket.</span><span class="sxs-lookup"><span data-stu-id="30de2-129">Docker Hub provides Docker image hosting, public or private registries, build triggers and web hooks, and integration with GitHub and Bitbucket.</span></span>

<span data-ttu-id="30de2-130">**Azure контейнер реестра**: общих ресурсов для работы с Docker images и его компонентов в Azure.</span><span class="sxs-lookup"><span data-stu-id="30de2-130">**Azure Container Registry**: A public resource for working with Docker images and its components in Azure.</span></span> <span data-ttu-id="30de2-131">Это обеспечивает реестра, который близок к развертываниям в Azure и, позволяет контролировать доступ, что позволяет использовать группы Azure Active Directory и разрешения.</span><span class="sxs-lookup"><span data-stu-id="30de2-131">This provides a registry that is close to your deployments in Azure and that gives you control over access, making it possible to use your Azure Active Directory groups and permissions.</span></span>

<span data-ttu-id="30de2-132">**Доверенный реестр docker (DTR)**: Служба реестра Docker (из Docker), может быть установлен локально, поэтому он размещается в центре обработки данных и сети организации.</span><span class="sxs-lookup"><span data-stu-id="30de2-132">**Docker Trusted Registry (DTR)**: A Docker registry service (from Docker) that can be installed on-premises so it lives within the organization’s datacenter and network.</span></span> <span data-ttu-id="30de2-133">Это удобно для частных образов, которые должны управляться в пределах предприятия.</span><span class="sxs-lookup"><span data-stu-id="30de2-133">It is convenient for private images that should be managed within the enterprise.</span></span> <span data-ttu-id="30de2-134">Доверенный реестр docker включен в состав продукта Docker центра обработки данных.</span><span class="sxs-lookup"><span data-stu-id="30de2-134">Docker Trusted Registry is included as part of the Docker Datacenter product.</span></span> <span data-ttu-id="30de2-135">Дополнительные сведения см. в разделе [доверенный реестр Docker (DTR)](https://docs.docker.com/docker-trusted-registry/overview/).</span><span class="sxs-lookup"><span data-stu-id="30de2-135">For more information, see [Docker Trusted Registry (DTR)](https://docs.docker.com/docker-trusted-registry/overview/).</span></span>

<span data-ttu-id="30de2-136">**Docker Community Edition (CE)**: средства разработки для Windows и macOS для сборки, запуск и тестирование в контейнер локально.</span><span class="sxs-lookup"><span data-stu-id="30de2-136">**Docker Community Edition (CE)**: Development tools for Windows and macOS for building, running, and testing containers locally.</span></span> <span data-ttu-id="30de2-137">CE docker для Windows предоставляет сред разработки для Linux и контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="30de2-137">Docker CE for Windows provides development environments for both Linux and Windows Containers.</span></span> <span data-ttu-id="30de2-138">На основе узла Linux Docker на Windows [Hyper-V](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="30de2-138">The Linux Docker host on Windows is based on a [Hyper-V](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) virtual machine.</span></span> <span data-ttu-id="30de2-139">Узел для контейнеров Windows непосредственно на основе окон.</span><span class="sxs-lookup"><span data-stu-id="30de2-139">The host for Windows Containers is directly based on Windows.</span></span> <span data-ttu-id="30de2-140">Docker CE для Mac основана на платформе низкоуровневой оболочки Apple и [низкоуровневой оболочки xhyve](https://github.com/mist64/xhyve), предоставляющее узла виртуальной машины Linux Docker, Mac OS X. Docker CE для Windows и для Mac заменяет элементов Docker, чтобы была основана Oracle VirtualBox.</span><span class="sxs-lookup"><span data-stu-id="30de2-140">Docker CE for Mac is based on the Apple Hypervisor framework and the [xhyve hypervisor](https://github.com/mist64/xhyve), which provides a Linux Docker host virtual machine on Mac OS X. Docker CE for Windows and for Mac replaces Docker Toolbox, which was based on Oracle VirtualBox.</span></span>

<span data-ttu-id="30de2-141">**Docker Enterprise Edition (EE)**: версия корпоративного уровня Docker средств для разработки приложений Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="30de2-141">**Docker Enterprise Edition (EE)**: An enterprise-scale version of Docker tools for Linux and Windows development.</span></span>

<span data-ttu-id="30de2-142">**Составить**: средство командной строки и YAML файл форматирования с метаданными для определения и запуска приложений несколькими контейнера.</span><span class="sxs-lookup"><span data-stu-id="30de2-142">**Compose**: A command-line tool and YAML file format with metadata for defining and running multi-container applications.</span></span> <span data-ttu-id="30de2-143">Можно определить одно приложение на основе нескольких образов с одного или нескольких файлов .yml, которые можно изменить значения в зависимости от среды.</span><span class="sxs-lookup"><span data-stu-id="30de2-143">You define a single application based on multiple images with one or more .yml files that can override values depending on the environment.</span></span> <span data-ttu-id="30de2-144">После создания определения можно развернуть приложение всего несколькими контейнера с помощью одной команды (docker-составления вверх), создает контейнер на изображение на узле Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-144">After you have created the definitions, you can deploy the whole multi-container application with a single command (docker-compose up) that creates a container per image on the Docker host.</span></span>

<span data-ttu-id="30de2-145">**Кластер**: коллекции узлов Docker, предоставляемых как если бы это был один виртуальный узел Docker, чтобы масштабировать приложение на нескольких экземплярах служб распределены по нескольким узлам кластера.</span><span class="sxs-lookup"><span data-stu-id="30de2-145">**Cluster**: A collection of Docker hosts exposed as if it were a single virtual Docker host, so that the application can scale to multiple instances of the services spread across multiple hosts within the cluster.</span></span> <span data-ttu-id="30de2-146">Docker кластеры могут создаваться с помощью Docker Swarm, Mesosphere DC/OS, Kubernetes и Azure Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30de2-146">Docker clusters can be created with Docker Swarm, Mesosphere DC/OS, Kubernetes, and Azure Service Fabric.</span></span> <span data-ttu-id="30de2-147">(Если вы используете помощью Docker Swarm по управлению кластером обычно обратитесь к кластеру как *скапливаются* вместо кластера.)</span><span class="sxs-lookup"><span data-stu-id="30de2-147">(If you use Docker Swarm for managing a cluster, you typically refer to the cluster as a *swarm* instead of a cluster.)</span></span>

<span data-ttu-id="30de2-148">**Orchestrator**: это средство, которое упрощает управление кластерами и узлами Docker.</span><span class="sxs-lookup"><span data-stu-id="30de2-148">**Orchestrator**: A tool that simplifies management of clusters and Docker hosts.</span></span> <span data-ttu-id="30de2-149">Orchestrators позволяют управлять их образы, контейнеры и узлами с помощью командной строки (CLI) или графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="30de2-149">Orchestrators enable you to manage their images, containers, and hosts through a command line interface (CLI) or a graphical UI.</span></span> <span data-ttu-id="30de2-150">Можно управлять сетевые подключения контейнеров, конфигурации, балансировки нагрузки, обнаружение служб, высокий уровень доступности, конфигурации узла Docker и многое другое.</span><span class="sxs-lookup"><span data-stu-id="30de2-150">You can manage container networking, configurations, load balancing, service discovery, high availability, Docker host configuration, and more.</span></span> <span data-ttu-id="30de2-151">Модуль отвечает за выполнение, распространение, масштабирование и восстановление рабочих нагрузок по набору узлов.</span><span class="sxs-lookup"><span data-stu-id="30de2-151">An orchestrator is responsible for running, distributing, scaling, and healing workloads across a collection of nodes.</span></span> <span data-ttu-id="30de2-152">Как правило orchestrator продуктов, которые одинаковые продукты, которые обеспечивают инфраструктуру кластера, например Mesosphere DC/OS, Kubernetes, помощью Docker Swarm и Azure Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30de2-152">Typically, orchestrator products are the same products that provide cluster infrastructure, like Mesosphere DC/OS, Kubernetes, Docker Swarm, and Azure Service Fabric.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="30de2-153">[Предыдущие] docker (defined.md) [Далее] (docker контейнеров — образы registries.md)</span><span class="sxs-lookup"><span data-stu-id="30de2-153">[Previous] (docker-defined.md) [Next] (docker-containers-images-registries.md)</span></span>