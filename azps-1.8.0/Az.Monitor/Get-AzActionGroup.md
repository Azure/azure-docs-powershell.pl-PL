---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 36d6a7ecb37338b12b68a37b07121a6ff376dd24
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403191"
---
# <span data-ttu-id="933db-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="933db-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="933db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="933db-102">SYNOPSIS</span></span>
<span data-ttu-id="933db-103">Pobiera grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="933db-103">Gets action group(s).</span></span>

## <span data-ttu-id="933db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="933db-104">SYNTAX</span></span>

### <span data-ttu-id="933db-105">BySubscriptionOrResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="933db-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933db-106">ByName</span><span class="sxs-lookup"><span data-stu-id="933db-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="933db-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="933db-107">DESCRIPTION</span></span>
<span data-ttu-id="933db-108">Polecenie **cmdlet Get-AzActionGroup** pobiera jedną lub więcej grup akcji.</span><span class="sxs-lookup"><span data-stu-id="933db-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="933db-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="933db-109">EXAMPLES</span></span>

### <span data-ttu-id="933db-110">Przykład 1. Uzyskiwanie grupy akcji według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="933db-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="933db-111">To polecenie zawiera listę wszystkich grup akcji dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="933db-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="933db-112">Przykład 2. Uzyskiwanie grup akcji dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="933db-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="933db-113">To polecenie zawiera listę grup akcji dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="933db-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="933db-114">Przykład 3. Uzyskiwanie grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="933db-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="933db-115">To polecenie wyświetla jedną grupę akcji (listę z jednym elementem).</span><span class="sxs-lookup"><span data-stu-id="933db-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="933db-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="933db-116">PARAMETERS</span></span>

### <span data-ttu-id="933db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933db-117">-DefaultProfile</span></span>
<span data-ttu-id="933db-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="933db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="933db-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="933db-119">-Name</span></span>
<span data-ttu-id="933db-120">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="933db-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933db-121">-ResourceGroupName</span></span>
<span data-ttu-id="933db-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="933db-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933db-123">CommonParameters</span></span>
<span data-ttu-id="933db-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933db-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="933db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933db-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933db-126">INPUTS</span></span>

### <span data-ttu-id="933db-127">System.String</span><span class="sxs-lookup"><span data-stu-id="933db-127">System.String</span></span>

## <span data-ttu-id="933db-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="933db-128">OUTPUTS</span></span>

### <span data-ttu-id="933db-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="933db-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="933db-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="933db-130">NOTES</span></span>

## <span data-ttu-id="933db-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="933db-131">RELATED LINKS</span></span>

<span data-ttu-id="933db-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="933db-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
