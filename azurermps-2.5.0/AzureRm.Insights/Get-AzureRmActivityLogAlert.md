---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: af8ef3ef2662dc6793011741fdfd7a903eaa081f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899337"
---
# <span data-ttu-id="a5c94-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a5c94-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a5c94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5c94-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c94-103">Pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a5c94-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5c94-104">SYNTAX</span></span>

### <span data-ttu-id="a5c94-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5c94-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5c94-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5c94-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5c94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a5c94-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c94-108">Polecenie cmdlet **Get-AzureRmActivityLogAlert** pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a5c94-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="a5c94-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5c94-109">EXAMPLES</span></span>

### <span data-ttu-id="a5c94-110">Przykład 1: uzyskiwanie alertów dziennika aktywności według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a5c94-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="a5c94-111">To polecenie wyświetla listę wszystkich alertów dziennika aktywności dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5c94-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="a5c94-112">Przykład 2: uzyskiwanie alertów dziennika aktywności dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a5c94-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="a5c94-113">To polecenie wyświetla listę alertów dziennika aktywności dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5c94-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="a5c94-114">Przykład 3: uzyskiwanie alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a5c94-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="a5c94-115">To polecenie wyświetla listę (listę z jednym elementem) alertem dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a5c94-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="a5c94-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5c94-116">PARAMETERS</span></span>

### <span data-ttu-id="a5c94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c94-117">-DefaultProfile</span></span>
<span data-ttu-id="a5c94-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a5c94-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c94-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5c94-119">-Name</span></span>
<span data-ttu-id="a5c94-120">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a5c94-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c94-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c94-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5c94-122">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="a5c94-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="a5c94-123">Jeśli nazwa nie ma wartości null lub jest pusta, ten parametr musi zawierać i nie być pustym ciągiem.</span><span class="sxs-lookup"><span data-stu-id="a5c94-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c94-124">CommonParameters</span></span>
<span data-ttu-id="a5c94-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c94-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c94-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5c94-127">INPUTS</span></span>

### <span data-ttu-id="a5c94-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c94-128">System.String</span></span>

## <span data-ttu-id="a5c94-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5c94-129">OUTPUTS</span></span>

### <span data-ttu-id="a5c94-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a5c94-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a5c94-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5c94-131">NOTES</span></span>

## <span data-ttu-id="a5c94-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5c94-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5c94-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a5c94-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)



[<span data-ttu-id="a5c94-134">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a5c94-134">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a5c94-135">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5c94-135">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a5c94-136">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a5c94-136">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
