---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 30635aa9bc1906c9e329e605327df1a2dfce5df4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526906"
---
# <span data-ttu-id="61092-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="61092-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="61092-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61092-102">SYNOPSIS</span></span>
<span data-ttu-id="61092-103">Umożliwia utworzenie grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="61092-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61092-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61092-104">SYNTAX</span></span>

### <span data-ttu-id="61092-105">CreateContainerGroupBaseParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61092-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61092-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="61092-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61092-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61092-107">DESCRIPTION</span></span>
<span data-ttu-id="61092-108">Polecenia cmdlet **New-AzureRmContainerGroup** tworzą grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="61092-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="61092-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61092-109">EXAMPLES</span></span>

### <span data-ttu-id="61092-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61092-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-111">To polecenie tworzy grupę kontenerów przy użyciu najnowszego obrazu Nginx i żąda publicznego adresu IP z otwartym portem 8000.</span><span class="sxs-lookup"><span data-stu-id="61092-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="61092-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="61092-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-113">To polecenie powoduje utworzenie grupy kontenerów i uruchomienie niestandardowego skryptu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="61092-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="61092-114">Przykład 3: Tworzenie grupy kontenerów uruchamianie-ukończenie.</span><span class="sxs-lookup"><span data-stu-id="61092-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-115">To polecenie tworzy grupę kontenerów, w której zostanie wydrukowany "cześć" i zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="61092-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="61092-116">Przykład 4: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze kontenera platformy Azure</span><span class="sxs-lookup"><span data-stu-id="61092-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-117">To polecenie tworzy grupę kontenerów przy użyciu obrazu Nginx w rejestrze kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61092-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="61092-118">Przykład 5: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze niestandardowego obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="61092-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-119">To polecenie tworzy grupę kontenerów przy użyciu obrazu niestandardowego z rejestru niestandardowego obrazu kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="61092-120">Przykład 6: Tworzenie grupy kontenerów instalujących wolumin plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="61092-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="61092-121">To polecenie tworzy grupę kontenerów, która instaluje udostępniony udział plików w usłudze Azure `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="61092-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="61092-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61092-122">PARAMETERS</span></span>

### <span data-ttu-id="61092-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="61092-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="61092-124">Poświadczenie konta magazynu w udziale plików platformy Azure do zainstalowania, gdzie nazwa użytkownika jest nazwą konta magazynu, a kluczem jest klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="61092-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="61092-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="61092-126">Ścieżka instalacji dla woluminu plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61092-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="61092-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="61092-128">Nazwa udziału plików platformy Azure do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="61092-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-129">-Command</span><span class="sxs-lookup"><span data-stu-id="61092-129">-Command</span></span>
<span data-ttu-id="61092-130">Polecenie, które ma zostać uruchomione w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="61092-130">The command to run in the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-131">-Procesor</span><span class="sxs-lookup"><span data-stu-id="61092-131">-Cpu</span></span>
<span data-ttu-id="61092-132">Wymagane rdzenie procesora.</span><span class="sxs-lookup"><span data-stu-id="61092-132">The required CPU cores.</span></span>
<span data-ttu-id="61092-133">Wartość domyślna: 1</span><span class="sxs-lookup"><span data-stu-id="61092-133">Default: 1</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61092-134">-DefaultProfile</span></span>
<span data-ttu-id="61092-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61092-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="61092-136">-DnsNameLabel</span></span>
<span data-ttu-id="61092-137">Etykieta nazwy DNS dla adresu IP.</span><span class="sxs-lookup"><span data-stu-id="61092-137">The DNS name label for the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="61092-138">-EnvironmentVariable</span></span>
<span data-ttu-id="61092-139">Zmienne środowiskowe kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-139">The container environment variables.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-140">-Image</span><span class="sxs-lookup"><span data-stu-id="61092-140">-Image</span></span>
<span data-ttu-id="61092-141">Obraz kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-141">The container image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-142">-Adres_iptype</span><span class="sxs-lookup"><span data-stu-id="61092-142">-IpAddressType</span></span>
<span data-ttu-id="61092-143">Typ adresu IP.</span><span class="sxs-lookup"><span data-stu-id="61092-143">The IP address type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="61092-144">-Location</span></span>
<span data-ttu-id="61092-145">Lokalizacja grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="61092-145">The container group Location.</span></span>
<span data-ttu-id="61092-146">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61092-146">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="61092-147">-MemoryInGB</span></span>
<span data-ttu-id="61092-148">Wymagana pamięć w GB.</span><span class="sxs-lookup"><span data-stu-id="61092-148">The required memory in GB.</span></span>
<span data-ttu-id="61092-149">Wartość domyślna: 1,5</span><span class="sxs-lookup"><span data-stu-id="61092-149">Default: 1.5</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61092-150">-Name</span></span>
<span data-ttu-id="61092-151">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="61092-151">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61092-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="61092-152">-OsType</span></span>
<span data-ttu-id="61092-153">Typ systemu operacyjnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-153">The container OS type.</span></span>
<span data-ttu-id="61092-154">Wartość domyślna: Linux</span><span class="sxs-lookup"><span data-stu-id="61092-154">Default: Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-155">-Port</span><span class="sxs-lookup"><span data-stu-id="61092-155">-Port</span></span>
<span data-ttu-id="61092-156">Liczba portów do otwarcia.</span><span class="sxs-lookup"><span data-stu-id="61092-156">The port(s) to open.</span></span> <span data-ttu-id="61092-157">Wartość domyślna: [80]</span><span class="sxs-lookup"><span data-stu-id="61092-157">Default: [80]</span></span>

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="61092-158">-RegistryCredential</span></span>
<span data-ttu-id="61092-159">Poświadczenia rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-159">The custom container registry credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="61092-160">-RegistryServerDomain</span></span>
<span data-ttu-id="61092-161">Serwer logowania rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-161">The custom container registry login server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61092-162">-ResourceGroupName</span></span>
<span data-ttu-id="61092-163">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61092-163">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61092-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="61092-164">-RestartPolicy</span></span>
<span data-ttu-id="61092-165">Zasady ponownego uruchamiania kontenera.</span><span class="sxs-lookup"><span data-stu-id="61092-165">The container restart policy.</span></span> <span data-ttu-id="61092-166">Domyślne: zawsze</span><span class="sxs-lookup"><span data-stu-id="61092-166">Default: Always</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="61092-167">-Tag</span></span>
<span data-ttu-id="61092-168">{{Opis znacznika Fill}}</span><span class="sxs-lookup"><span data-stu-id="61092-168">{{Fill Tag Description}}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61092-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61092-169">-Confirm</span></span>
<span data-ttu-id="61092-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61092-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61092-171">-WhatIf</span></span>
<span data-ttu-id="61092-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61092-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61092-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61092-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61092-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61092-174">CommonParameters</span></span>
<span data-ttu-id="61092-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61092-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61092-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61092-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61092-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61092-177">INPUTS</span></span>

### <span data-ttu-id="61092-178">System. String</span><span class="sxs-lookup"><span data-stu-id="61092-178">System.String</span></span>
<span data-ttu-id="61092-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="61092-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="61092-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61092-180">OUTPUTS</span></span>

### <span data-ttu-id="61092-181">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="61092-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="61092-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61092-182">NOTES</span></span>

## <span data-ttu-id="61092-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61092-183">RELATED LINKS</span></span>
