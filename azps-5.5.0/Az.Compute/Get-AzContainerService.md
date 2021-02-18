---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181739"
---
# <span data-ttu-id="baf1d-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="baf1d-101">Get-AzContainerService</span></span>

## <span data-ttu-id="baf1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="baf1d-103">Pobiera usługę kontenerową.</span><span class="sxs-lookup"><span data-stu-id="baf1d-103">Gets a container service.</span></span>

## <span data-ttu-id="baf1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="baf1d-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baf1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="baf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="baf1d-106">Polecenie **cmdlet Get-AzContainerService** pobiera usługę kontenerową.</span><span class="sxs-lookup"><span data-stu-id="baf1d-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="baf1d-107">Możesz wyświetlić właściwości usługi kontenerowej, takie jak województwo, liczba wzorców i agentów oraz w pełni kwalifikowana nazwa domeny wzorca i agenta.</span><span class="sxs-lookup"><span data-stu-id="baf1d-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="baf1d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="baf1d-108">EXAMPLES</span></span>

### <span data-ttu-id="baf1d-109">Przykład 1. Uzyskiwanie usługi kontenerowej</span><span class="sxs-lookup"><span data-stu-id="baf1d-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="baf1d-110">To polecenie pobiera usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="baf1d-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="baf1d-111">Przykład 2. Uzyskiwanie wszystkich usług kontenerowych</span><span class="sxs-lookup"><span data-stu-id="baf1d-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="baf1d-112">To polecenie pobiera wszystkie usługi kontenerów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="baf1d-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="baf1d-113">Przykład 3. Uzyskiwanie wszystkich usług kontenerowych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="baf1d-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="baf1d-114">To polecenie pobiera wszystkie usługi kontenerów w grupie ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="baf1d-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="baf1d-115">Przykład 4. Uzyskiwanie wszystkich usług kontenerów przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="baf1d-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="baf1d-116">To polecenie pobiera wszystkie usługi kontenerów zaczynające się od "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="baf1d-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="baf1d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf1d-117">PARAMETERS</span></span>

### <span data-ttu-id="baf1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf1d-118">-DefaultProfile</span></span>
<span data-ttu-id="baf1d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="baf1d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="baf1d-120">-Name</span></span>
<span data-ttu-id="baf1d-121">Określa nazwę usługi kontenerów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf1d-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="baf1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="baf1d-123">Określa grupę zasobów usługi kontenerów, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf1d-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="baf1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf1d-124">CommonParameters</span></span>
<span data-ttu-id="baf1d-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf1d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf1d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf1d-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf1d-127">INPUTS</span></span>

### <span data-ttu-id="baf1d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="baf1d-128">System.String</span></span>

## <span data-ttu-id="baf1d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="baf1d-129">OUTPUTS</span></span>

### <span data-ttu-id="baf1d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="baf1d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="baf1d-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="baf1d-131">NOTES</span></span>

## <span data-ttu-id="baf1d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baf1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="baf1d-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="baf1d-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="baf1d-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="baf1d-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="baf1d-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="baf1d-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


