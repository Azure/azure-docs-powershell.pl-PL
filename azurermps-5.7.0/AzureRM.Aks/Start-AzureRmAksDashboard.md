---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717766"
---
# <span data-ttu-id="05599-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="05599-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="05599-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05599-102">SYNOPSIS</span></span>
<span data-ttu-id="05599-103">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="05599-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05599-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05599-104">SYNTAX</span></span>

### <span data-ttu-id="05599-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05599-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05599-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05599-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05599-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05599-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05599-108">Opis</span><span class="sxs-lookup"><span data-stu-id="05599-108">DESCRIPTION</span></span>
<span data-ttu-id="05599-109">Utwórz tunel SSH Kubectl na pulpicie nawigacyjnym zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="05599-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="05599-110">Tunel SSH jest skonfigurowany w zadaniu programu PowerShell o nazwie Kubectl-Tunnel i można go znaleźć, uruchamiając `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="05599-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="05599-111">Tunel powinien być dostępny za pośrednictwem [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="05599-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="05599-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05599-112">EXAMPLES</span></span>

### <span data-ttu-id="05599-113">Rozpoczynanie tunelu SSH i otwieranie przeglądarki na pulpicie nawigacyjnym Kubernetes</span><span class="sxs-lookup"><span data-stu-id="05599-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="05599-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05599-114">PARAMETERS</span></span>

### <span data-ttu-id="05599-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05599-115">-DefaultProfile</span></span>
<span data-ttu-id="05599-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05599-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05599-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="05599-117">-DisableBrowser</span></span>
<span data-ttu-id="05599-118">Nie otwieraj przeglądarki po establising kubectl port-forward.</span><span class="sxs-lookup"><span data-stu-id="05599-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05599-119">-ID</span><span class="sxs-lookup"><span data-stu-id="05599-119">-Id</span></span>
<span data-ttu-id="05599-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="05599-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05599-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05599-121">-InputObject</span></span>
<span data-ttu-id="05599-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="05599-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05599-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05599-123">-Name</span></span>
<span data-ttu-id="05599-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="05599-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05599-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05599-125">-PassThru</span></span>
<span data-ttu-id="05599-126">Polecenie cmdlet zwraca wartość KubeTunnelJob, jeśli została przekazana.</span><span class="sxs-lookup"><span data-stu-id="05599-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05599-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05599-127">-ResourceGroupName</span></span>
<span data-ttu-id="05599-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="05599-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05599-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05599-129">CommonParameters</span></span>
<span data-ttu-id="05599-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05599-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05599-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05599-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05599-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05599-132">INPUTS</span></span>

### <span data-ttu-id="05599-133">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="05599-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="05599-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05599-134">System.String</span></span>

## <span data-ttu-id="05599-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05599-135">OUTPUTS</span></span>

### <span data-ttu-id="05599-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="05599-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="05599-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05599-137">NOTES</span></span>

## <span data-ttu-id="05599-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05599-138">RELATED LINKS</span></span>
