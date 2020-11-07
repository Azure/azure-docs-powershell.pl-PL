---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 42ef63d9884cef45b107b9c959b264402e4347d1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891214"
---
# <span data-ttu-id="fa6f4-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fa6f4-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="fa6f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6f4-103">Pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="fa6f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa6f4-104">SYNTAX</span></span>

### <span data-ttu-id="fa6f4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa6f4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa6f4-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa6f4-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa6f4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa6f4-107">DESCRIPTION</span></span>
<span data-ttu-id="fa6f4-108">Polecenie cmdlet **Get-AzActivityLogAlert** pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="fa6f4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa6f4-109">EXAMPLES</span></span>

### <span data-ttu-id="fa6f4-110">Przykład 1: uzyskiwanie alertów dziennika aktywności według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fa6f4-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="fa6f4-111">To polecenie wyświetla listę wszystkich alertów dziennika aktywności dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="fa6f4-112">Przykład 2: uzyskiwanie alertów dziennika aktywności dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fa6f4-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="fa6f4-113">To polecenie wyświetla listę alertów dziennika aktywności dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="fa6f4-114">Przykład 3: uzyskiwanie alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="fa6f4-115">To polecenie wyświetla listę (listę z jednym elementem) alertem dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="fa6f4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa6f4-116">PARAMETERS</span></span>

### <span data-ttu-id="fa6f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6f4-117">-DefaultProfile</span></span>
<span data-ttu-id="fa6f4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fa6f4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa6f4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa6f4-119">-Name</span></span>
<span data-ttu-id="fa6f4-120">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="fa6f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa6f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="fa6f4-122">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="fa6f4-123">Jeśli nazwa nie ma wartości null lub jest pusta, ten parametr musi zawierać i nie być pustym ciągiem.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="fa6f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6f4-124">CommonParameters</span></span>
<span data-ttu-id="fa6f4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6f4-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa6f4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6f4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa6f4-127">INPUTS</span></span>

### <span data-ttu-id="fa6f4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fa6f4-128">System.String</span></span>

## <span data-ttu-id="fa6f4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa6f4-129">OUTPUTS</span></span>

### <span data-ttu-id="fa6f4-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="fa6f4-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="fa6f4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa6f4-131">NOTES</span></span>

## <span data-ttu-id="fa6f4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa6f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa6f4-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fa6f4-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="fa6f4-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fa6f4-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="fa6f4-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fa6f4-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="fa6f4-136">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="fa6f4-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="fa6f4-137">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="fa6f4-137">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
