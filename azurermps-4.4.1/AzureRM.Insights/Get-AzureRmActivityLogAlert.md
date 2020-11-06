---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553865"
---
# <span data-ttu-id="649a7-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="649a7-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="649a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="649a7-102">SYNOPSIS</span></span>
<span data-ttu-id="649a7-103">Pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="649a7-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="649a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="649a7-104">SYNTAX</span></span>

### <span data-ttu-id="649a7-105">Domyślne parametry pobierania alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="649a7-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="649a7-106">Parametry, aby upewnić się, że grupa zasobów jest podana po podanej nazwie</span><span class="sxs-lookup"><span data-stu-id="649a7-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="649a7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="649a7-107">DESCRIPTION</span></span>
<span data-ttu-id="649a7-108">Polecenie cmdlet **Get-AzureRmActivityLogAlert** pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="649a7-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="649a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="649a7-109">EXAMPLES</span></span>

### <span data-ttu-id="649a7-110">Przykład 1: uzyskiwanie alertów dziennika aktywności według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="649a7-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="649a7-111">To polecenie wyświetla listę wszystkich alertów dziennika aktywności dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="649a7-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="649a7-112">Przykład 2: uzyskiwanie alertów dziennika aktywności dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="649a7-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="649a7-113">To polecenie wyświetla listę alertów dziennika aktywności dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="649a7-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="649a7-114">Przykład 3: uzyskiwanie alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="649a7-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="649a7-115">To polecenie wyświetla listę (listę z jednym elementem) alertem dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="649a7-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="649a7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="649a7-116">PARAMETERS</span></span>

### <span data-ttu-id="649a7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="649a7-117">-Name</span></span>
<span data-ttu-id="649a7-118">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="649a7-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="649a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="649a7-120">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="649a7-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="649a7-121">Jeśli nazwa nie ma wartości null lub jest pusta, ten parametr musi zawierać i nie być pustym ciągiem.</span><span class="sxs-lookup"><span data-stu-id="649a7-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649a7-122">-DefaultProfile</span></span>
<span data-ttu-id="649a7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="649a7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="649a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649a7-124">CommonParameters</span></span>
<span data-ttu-id="649a7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="649a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649a7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="649a7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649a7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="649a7-127">INPUTS</span></span>

### <span data-ttu-id="649a7-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="649a7-128">None</span></span>

## <span data-ttu-id="649a7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="649a7-129">OUTPUTS</span></span>

### <span data-ttu-id="649a7-130"><system. Collections. Generic. list "1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="649a7-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="649a7-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="649a7-131">None</span></span>

## <span data-ttu-id="649a7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="649a7-132">NOTES</span></span>

## <span data-ttu-id="649a7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="649a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="649a7-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="649a7-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="649a7-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="649a7-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="649a7-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="649a7-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="649a7-137">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="649a7-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="649a7-138">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="649a7-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
