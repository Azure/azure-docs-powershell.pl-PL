---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050179"
---
# <span data-ttu-id="ed534-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="ed534-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="ed534-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed534-102">SYNOPSIS</span></span>
<span data-ttu-id="ed534-103">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="ed534-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="ed534-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed534-104">SYNTAX</span></span>

### <span data-ttu-id="ed534-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed534-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed534-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed534-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed534-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed534-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed534-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ed534-108">DESCRIPTION</span></span>
<span data-ttu-id="ed534-109">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="ed534-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="ed534-110">Tunel SSH jest skonfigurowany w zadaniu programu PowerShell o nazwie Kubectl-Tunnel i można go znaleźć, uruchamiając `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="ed534-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="ed534-111">Tunel powinien być dostępny za pośrednictwem [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="ed534-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="ed534-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed534-112">EXAMPLES</span></span>

### <span data-ttu-id="ed534-113">Rozpoczynanie tunelu SSH i otwieranie przeglądarki na pulpicie nawigacyjnym Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed534-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ed534-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed534-114">PARAMETERS</span></span>

### <span data-ttu-id="ed534-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed534-115">-DefaultProfile</span></span>
<span data-ttu-id="ed534-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed534-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed534-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="ed534-117">-DisableBrowser</span></span>
<span data-ttu-id="ed534-118">Nie otwieraj przeglądarki po ustanowieniu kubectl port do przodu.</span><span class="sxs-lookup"><span data-stu-id="ed534-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ed534-119">-Id</span></span>
<span data-ttu-id="ed534-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed534-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ed534-121">-InputObject</span></span>
<span data-ttu-id="ed534-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ed534-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed534-123">-Name</span></span>
<span data-ttu-id="ed534-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed534-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed534-125">-PassThru</span></span>
<span data-ttu-id="ed534-126">Polecenie cmdlet zwraca wartość KubeTunnelJob, jeśli została przekazana.</span><span class="sxs-lookup"><span data-stu-id="ed534-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed534-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed534-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ed534-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed534-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed534-129">CommonParameters</span></span>
<span data-ttu-id="ed534-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed534-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed534-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed534-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed534-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed534-132">INPUTS</span></span>

### <span data-ttu-id="ed534-133">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ed534-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ed534-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed534-134">System.String</span></span>

## <span data-ttu-id="ed534-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed534-135">OUTPUTS</span></span>

### <span data-ttu-id="ed534-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="ed534-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="ed534-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed534-137">NOTES</span></span>

## <span data-ttu-id="ed534-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed534-138">RELATED LINKS</span></span>
