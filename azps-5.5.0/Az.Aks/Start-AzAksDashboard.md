---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199834"
---
# <span data-ttu-id="cb451-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="cb451-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="cb451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb451-102">SYNOPSIS</span></span>
<span data-ttu-id="cb451-103">Utwórz podskok SSH firmy Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="cb451-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="cb451-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb451-104">SYNTAX</span></span>

### <span data-ttu-id="cb451-105">GroupNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cb451-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb451-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb451-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb451-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb451-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb451-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb451-108">DESCRIPTION</span></span>
<span data-ttu-id="cb451-109">Utwórz podskok SSH firmy Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="cb451-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="cb451-110">Podkoszowy SSH jest konfigurowany w zadaniu programu PowerShell o nazwie Kubectl-Tunnel można go znaleźć po `Get-Job` uruchomieniu.</span><span class="sxs-lookup"><span data-stu-id="cb451-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="cb451-111">Ten podjadek powinien być dostępny za [http://127.0.0.1:8001](http://127.0.0.1:8001) pośrednictwem.</span><span class="sxs-lookup"><span data-stu-id="cb451-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="cb451-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb451-112">EXAMPLES</span></span>

### <span data-ttu-id="cb451-113">Rozpoczynanie pracy z panelem SSH i otwieranie przeglądarki na pulpicie nawigacyjnym Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cb451-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="cb451-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb451-114">PARAMETERS</span></span>

### <span data-ttu-id="cb451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb451-115">-DefaultProfile</span></span>
<span data-ttu-id="cb451-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb451-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb451-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="cb451-117">-DisableBrowser</span></span>
<span data-ttu-id="cb451-118">Nie otwieraj przeglądarki po nawiązyniu port-forward kubectl.</span><span class="sxs-lookup"><span data-stu-id="cb451-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="cb451-119">— Id</span><span class="sxs-lookup"><span data-stu-id="cb451-119">-Id</span></span>
<span data-ttu-id="cb451-120">Identyfikator zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cb451-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="cb451-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb451-121">-InputObject</span></span>
<span data-ttu-id="cb451-122">Obiekt PSKubernetesCluster, który normalnie przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="cb451-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb451-123">- ListenPort</span><span class="sxs-lookup"><span data-stu-id="cb451-123">-ListenPort</span></span>
<span data-ttu-id="cb451-124">Port nasłuchiwania pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="cb451-124">The listening port for the dashboard.</span></span> <span data-ttu-id="cb451-125">Wartość domyślna to 8003.</span><span class="sxs-lookup"><span data-stu-id="cb451-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="cb451-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cb451-126">-Name</span></span>
<span data-ttu-id="cb451-127">Nazwa zarządzanego klastru Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cb451-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="cb451-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb451-128">-PassThru</span></span>
<span data-ttu-id="cb451-129">Polecenie cmdlet zwraca wartość błędu KubeTunnelJob, jeśli minął.</span><span class="sxs-lookup"><span data-stu-id="cb451-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="cb451-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb451-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb451-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cb451-131">Resource group name</span></span>

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

### <span data-ttu-id="cb451-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb451-132">CommonParameters</span></span>
<span data-ttu-id="cb451-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb451-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb451-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb451-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb451-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb451-135">INPUTS</span></span>

### <span data-ttu-id="cb451-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cb451-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="cb451-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cb451-137">System.String</span></span>

## <span data-ttu-id="cb451-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb451-138">OUTPUTS</span></span>

### <span data-ttu-id="cb451-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="cb451-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="cb451-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb451-140">NOTES</span></span>

## <span data-ttu-id="cb451-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb451-141">RELATED LINKS</span></span>
