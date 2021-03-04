---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981834"
---
# <span data-ttu-id="b5a31-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="b5a31-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="b5a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a31-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a31-103">Pobiera upuszczona kopia zapasowa puli sql dla puli składni Synapse Sql.</span><span class="sxs-lookup"><span data-stu-id="b5a31-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="b5a31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5a31-104">SYNTAX</span></span>

### <span data-ttu-id="b5a31-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b5a31-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a31-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="b5a31-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a31-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5a31-107">DESCRIPTION</span></span>
<span data-ttu-id="b5a31-108">Polecenie **cmdlet Get-AzSynapseDroppedSqlPool** pobiera określoną usuniętą kopię zapasową puli SQL, która można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b5a31-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="b5a31-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5a31-109">EXAMPLES</span></span>

### <span data-ttu-id="b5a31-110">Przykład 1. Uzyskiwanie określonych upuszczanych buforów sql z puli sql</span><span class="sxs-lookup"><span data-stu-id="b5a31-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="b5a31-111">Polecenie cmdlet pobiera upuszczane bufory sql dla puli sql.</span><span class="sxs-lookup"><span data-stu-id="b5a31-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="b5a31-112">Przykład 2. Uzyskiwanie całej usuniętej buforu sql w obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="b5a31-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="b5a31-113">To polecenie jest dostępne wszystkiego w upuszczanej bazie danych sqlpool w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b5a31-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="b5a31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5a31-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a31-115">-DefaultProfile</span></span>
<span data-ttu-id="b5a31-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a31-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b5a31-117">-Name</span></span>
<span data-ttu-id="b5a31-118">Pula języka Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="b5a31-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a31-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5a31-119">-ResourceId</span></span>
<span data-ttu-id="b5a31-120">Wprowadzanie usuniętego identyfikatora zasobu puli sql.</span><span class="sxs-lookup"><span data-stu-id="b5a31-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a31-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5a31-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5a31-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a31-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5a31-123">-WorkspaceName</span></span>
<span data-ttu-id="b5a31-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b5a31-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a31-125">CommonParameters</span></span>
<span data-ttu-id="b5a31-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a31-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5a31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a31-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5a31-128">INPUTS</span></span>

### <span data-ttu-id="b5a31-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5a31-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b5a31-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5a31-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="b5a31-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5a31-131">OUTPUTS</span></span>

### <span data-ttu-id="b5a31-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="b5a31-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="b5a31-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5a31-133">NOTES</span></span>

## <span data-ttu-id="b5a31-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5a31-134">RELATED LINKS</span></span>
