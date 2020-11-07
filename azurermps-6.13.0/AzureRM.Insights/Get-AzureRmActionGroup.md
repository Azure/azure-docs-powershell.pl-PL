---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717193"
---
# <span data-ttu-id="7a3ed-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7a3ed-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="7a3ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3ed-103">Pobiera grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a3ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a3ed-104">SYNTAX</span></span>

### <span data-ttu-id="7a3ed-105">BySubscriptionOrResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a3ed-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a3ed-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7a3ed-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a3ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a3ed-107">DESCRIPTION</span></span>
<span data-ttu-id="7a3ed-108">Polecenie cmdlet **Get-AzureRmActionGroup umożliwia pobranie** co najmniej jednej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="7a3ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a3ed-109">EXAMPLES</span></span>

### <span data-ttu-id="7a3ed-110">Przykład 1: Uzyskiwanie grupy akcji według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7a3ed-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="7a3ed-111">To polecenie umożliwia wyświetlenie listy wszystkich grup akcji dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="7a3ed-112">Przykład 2: pobieranie grup akcji dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a3ed-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="7a3ed-113">To polecenie wyświetla listę grup akcji dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="7a3ed-114">Przykład 3: Uzyskiwanie grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="7a3ed-115">To polecenie wyświetla listę (listę z pojedynczym elementem) grupą akcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="7a3ed-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a3ed-116">PARAMETERS</span></span>

### <span data-ttu-id="7a3ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3ed-117">-DefaultProfile</span></span>
<span data-ttu-id="7a3ed-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a3ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a3ed-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a3ed-119">-Name</span></span>
<span data-ttu-id="7a3ed-120">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-120">The name of the action group.</span></span>

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

### <span data-ttu-id="7a3ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a3ed-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a3ed-122">The resource group name</span></span>

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

### <span data-ttu-id="7a3ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3ed-123">CommonParameters</span></span>
<span data-ttu-id="7a3ed-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3ed-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a3ed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3ed-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a3ed-126">INPUTS</span></span>

### <span data-ttu-id="7a3ed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7a3ed-127">System.String</span></span>

## <span data-ttu-id="7a3ed-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a3ed-128">OUTPUTS</span></span>

### <span data-ttu-id="7a3ed-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="7a3ed-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="7a3ed-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a3ed-130">NOTES</span></span>

## <span data-ttu-id="7a3ed-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a3ed-131">RELATED LINKS</span></span>

<span data-ttu-id="7a3ed-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="7a3ed-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
