---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500482"
---
# <span data-ttu-id="503b2-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="503b2-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="503b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="503b2-102">SYNOPSIS</span></span>
<span data-ttu-id="503b2-103">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="503b2-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="503b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="503b2-104">SYNTAX</span></span>

### <span data-ttu-id="503b2-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="503b2-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="503b2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="503b2-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="503b2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="503b2-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="503b2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="503b2-108">DESCRIPTION</span></span>
<span data-ttu-id="503b2-109">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="503b2-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="503b2-110">Tunel SSH jest skonfigurowany w zadaniu programu PowerShell o nazwie Kubectl-Tunnel i można go znaleźć, uruchamiając `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="503b2-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="503b2-111">Tunel powinien być dostępny za pośrednictwem [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="503b2-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="503b2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="503b2-112">EXAMPLES</span></span>

### <span data-ttu-id="503b2-113">Rozpoczynanie tunelu SSH i otwieranie przeglądarki na pulpicie nawigacyjnym Kubernetes</span><span class="sxs-lookup"><span data-stu-id="503b2-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="503b2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="503b2-114">PARAMETERS</span></span>

### <span data-ttu-id="503b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503b2-115">-DefaultProfile</span></span>
<span data-ttu-id="503b2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="503b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="503b2-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="503b2-117">-DisableBrowser</span></span>
<span data-ttu-id="503b2-118">Nie otwieraj przeglądarki po ustanowieniu kubectl port do przodu.</span><span class="sxs-lookup"><span data-stu-id="503b2-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="503b2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="503b2-119">-Id</span></span>
<span data-ttu-id="503b2-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="503b2-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="503b2-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="503b2-121">-InputObject</span></span>
<span data-ttu-id="503b2-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="503b2-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="503b2-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="503b2-123">-ListenPort</span></span>
<span data-ttu-id="503b2-124">Port nasłuchujący pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="503b2-124">The listening port for the dashboard.</span></span> <span data-ttu-id="503b2-125">Wartość domyślna to 8003.</span><span class="sxs-lookup"><span data-stu-id="503b2-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="503b2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="503b2-126">-Name</span></span>
<span data-ttu-id="503b2-127">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="503b2-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="503b2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="503b2-128">-PassThru</span></span>
<span data-ttu-id="503b2-129">Polecenie cmdlet zwraca wartość KubeTunnelJob, jeśli została przekazana.</span><span class="sxs-lookup"><span data-stu-id="503b2-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="503b2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="503b2-130">-ResourceGroupName</span></span>
<span data-ttu-id="503b2-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="503b2-131">Resource group name</span></span>

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

### <span data-ttu-id="503b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503b2-132">CommonParameters</span></span>
<span data-ttu-id="503b2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="503b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503b2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="503b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503b2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="503b2-135">INPUTS</span></span>

### <span data-ttu-id="503b2-136">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="503b2-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="503b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="503b2-137">System.String</span></span>

## <span data-ttu-id="503b2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="503b2-138">OUTPUTS</span></span>

### <span data-ttu-id="503b2-139">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="503b2-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="503b2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="503b2-140">NOTES</span></span>

## <span data-ttu-id="503b2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="503b2-141">RELATED LINKS</span></span>
