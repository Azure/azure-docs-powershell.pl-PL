---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 31e36048587ba6faeee42ab1c2bf15afe1ae1e71
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398754"
---
# <span data-ttu-id="db030-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db030-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="db030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db030-102">SYNOPSIS</span></span>
<span data-ttu-id="db030-103">Pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="db030-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="db030-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db030-104">SYNTAX</span></span>

### <span data-ttu-id="db030-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db030-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db030-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db030-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db030-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="db030-107">DESCRIPTION</span></span>
<span data-ttu-id="db030-108">Polecenie **cmdlet Get-AzActivityLogAlert** pobiera jeden lub więcej zasobów alertów dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="db030-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="db030-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db030-109">EXAMPLES</span></span>

### <span data-ttu-id="db030-110">Przykład 1. Uzyskiwanie alertów dziennika aktywności według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="db030-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="db030-111">To polecenie zawiera listę wszystkich alertów dziennika aktywności dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db030-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="db030-112">Przykład 2. Uzyskiwanie alertów dziennika aktywności dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="db030-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="db030-113">To polecenie zawiera listę alertów dziennika aktywności dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db030-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="db030-114">Przykład 3. Uzyskiwanie alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="db030-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="db030-115">To polecenie wyświetla jeden alert (listę z jednym elementem) alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="db030-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="db030-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db030-116">PARAMETERS</span></span>

### <span data-ttu-id="db030-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db030-117">-DefaultProfile</span></span>
<span data-ttu-id="db030-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="db030-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db030-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="db030-119">-Name</span></span>
<span data-ttu-id="db030-120">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="db030-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="db030-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db030-121">-ResourceGroupName</span></span>
<span data-ttu-id="db030-122">Nazwa grupy zasobów, w której istnieje zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="db030-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="db030-123">Jeśli nazwa nie ma wartości null lub jest pusta, ten parametr musi zawierać ciąg niepusty.</span><span class="sxs-lookup"><span data-stu-id="db030-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="db030-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db030-124">CommonParameters</span></span>
<span data-ttu-id="db030-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db030-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db030-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db030-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db030-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db030-127">INPUTS</span></span>

### <span data-ttu-id="db030-128">System.String</span><span class="sxs-lookup"><span data-stu-id="db030-128">System.String</span></span>

## <span data-ttu-id="db030-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db030-129">OUTPUTS</span></span>

### <span data-ttu-id="db030-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="db030-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="db030-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db030-131">NOTES</span></span>

## <span data-ttu-id="db030-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db030-132">RELATED LINKS</span></span>

[<span data-ttu-id="db030-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db030-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="db030-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db030-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="db030-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="db030-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
