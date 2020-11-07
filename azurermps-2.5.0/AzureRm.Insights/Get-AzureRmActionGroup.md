---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899341"
---
# <span data-ttu-id="73f29-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="73f29-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="73f29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73f29-102">SYNOPSIS</span></span>
<span data-ttu-id="73f29-103">Pobiera grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73f29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73f29-104">SYNTAX</span></span>

### <span data-ttu-id="73f29-105">BySubscriptionOrResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73f29-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73f29-106">ByName</span><span class="sxs-lookup"><span data-stu-id="73f29-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73f29-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73f29-107">DESCRIPTION</span></span>
<span data-ttu-id="73f29-108">Polecenie cmdlet **Get-AzureRmActionGroup umożliwia pobranie** co najmniej jednej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="73f29-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73f29-109">EXAMPLES</span></span>

### <span data-ttu-id="73f29-110">Przykład 1: Uzyskiwanie grupy akcji według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="73f29-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="73f29-111">To polecenie umożliwia wyświetlenie listy wszystkich grup akcji dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="73f29-112">Przykład 2: pobieranie grup akcji dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73f29-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="73f29-113">To polecenie wyświetla listę grup akcji dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73f29-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="73f29-114">Przykład 3: Uzyskiwanie grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="73f29-115">To polecenie wyświetla listę (listę z pojedynczym elementem) grupą akcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="73f29-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73f29-116">PARAMETERS</span></span>

### <span data-ttu-id="73f29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f29-117">-DefaultProfile</span></span>
<span data-ttu-id="73f29-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="73f29-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73f29-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73f29-119">-Name</span></span>
<span data-ttu-id="73f29-120">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="73f29-120">The name of the action group.</span></span>

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

### <span data-ttu-id="73f29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f29-121">-ResourceGroupName</span></span>
<span data-ttu-id="73f29-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73f29-122">The resource group name</span></span>

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

### <span data-ttu-id="73f29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f29-123">CommonParameters</span></span>
<span data-ttu-id="73f29-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f29-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f29-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f29-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f29-126">INPUTS</span></span>

### <span data-ttu-id="73f29-127">System. String</span><span class="sxs-lookup"><span data-stu-id="73f29-127">System.String</span></span>

## <span data-ttu-id="73f29-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73f29-128">OUTPUTS</span></span>

### <span data-ttu-id="73f29-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="73f29-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="73f29-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73f29-130">NOTES</span></span>

## <span data-ttu-id="73f29-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f29-131">RELATED LINKS</span></span>

<span data-ttu-id="73f29-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="73f29-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
