---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362495"
---
# <span data-ttu-id="0951f-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="0951f-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="0951f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0951f-102">SYNOPSIS</span></span>
<span data-ttu-id="0951f-103">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="0951f-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="0951f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0951f-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0951f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0951f-105">DESCRIPTION</span></span>
<span data-ttu-id="0951f-106">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="0951f-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="0951f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0951f-107">EXAMPLES</span></span>

### <span data-ttu-id="0951f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0951f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="0951f-109">Śledzenie aktualizacji konserwacji zasobów</span><span class="sxs-lookup"><span data-stu-id="0951f-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="0951f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0951f-110">PARAMETERS</span></span>

### <span data-ttu-id="0951f-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="0951f-111">-ApplyUpdateName</span></span>
<span data-ttu-id="0951f-112">Nazwa zasobu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="0951f-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0951f-113">-DefaultProfile</span></span>
<span data-ttu-id="0951f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0951f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0951f-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="0951f-115">-ProviderName</span></span>
<span data-ttu-id="0951f-116">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0951f-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0951f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0951f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0951f-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0951f-119">-ResourceName</span></span>
<span data-ttu-id="0951f-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0951f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="0951f-121">-ResourceParentName</span></span>
<span data-ttu-id="0951f-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="0951f-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="0951f-123">-ResourceParentType</span></span>
<span data-ttu-id="0951f-124">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="0951f-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0951f-125">-ResourceType</span></span>
<span data-ttu-id="0951f-126">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="0951f-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0951f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0951f-127">CommonParameters</span></span>
<span data-ttu-id="0951f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0951f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0951f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0951f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0951f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0951f-130">INPUTS</span></span>

### <span data-ttu-id="0951f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0951f-131">System.String</span></span>

## <span data-ttu-id="0951f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0951f-132">OUTPUTS</span></span>

### <span data-ttu-id="0951f-133">Microsoft. Azure. Commands. Maintenance. models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="0951f-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="0951f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0951f-134">NOTES</span></span>

## <span data-ttu-id="0951f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0951f-135">RELATED LINKS</span></span>
