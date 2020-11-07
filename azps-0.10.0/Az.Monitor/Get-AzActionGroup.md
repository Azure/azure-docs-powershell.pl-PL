---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: ca4229f5f882b1065c6f39b8c162bb91b90b835d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891217"
---
# <span data-ttu-id="8a2ee-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8a2ee-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="8a2ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2ee-103">Pobiera grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-103">Gets action group(s).</span></span>

## <span data-ttu-id="8a2ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a2ee-104">SYNTAX</span></span>

### <span data-ttu-id="8a2ee-105">BySubscriptionOrResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a2ee-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a2ee-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8a2ee-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a2ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8a2ee-107">DESCRIPTION</span></span>
<span data-ttu-id="8a2ee-108">Polecenie cmdlet **Get-AzActionGroup umożliwia pobranie** co najmniej jednej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="8a2ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a2ee-109">EXAMPLES</span></span>

### <span data-ttu-id="8a2ee-110">Przykład 1: Uzyskiwanie grupy akcji według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8a2ee-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="8a2ee-111">To polecenie umożliwia wyświetlenie listy wszystkich grup akcji dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="8a2ee-112">Przykład 2: pobieranie grup akcji dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8a2ee-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="8a2ee-113">To polecenie wyświetla listę grup akcji dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="8a2ee-114">Przykład 3: Uzyskiwanie grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="8a2ee-115">To polecenie wyświetla listę (listę z pojedynczym elementem) grupą akcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="8a2ee-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a2ee-116">PARAMETERS</span></span>

### <span data-ttu-id="8a2ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2ee-117">-DefaultProfile</span></span>
<span data-ttu-id="8a2ee-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8a2ee-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a2ee-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a2ee-119">-Name</span></span>
<span data-ttu-id="8a2ee-120">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-120">The name of the action group.</span></span>

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

### <span data-ttu-id="8a2ee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2ee-121">-ResourceGroupName</span></span>
<span data-ttu-id="8a2ee-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8a2ee-122">The resource group name</span></span>

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

### <span data-ttu-id="8a2ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2ee-123">CommonParameters</span></span>
<span data-ttu-id="8a2ee-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2ee-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a2ee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2ee-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a2ee-126">INPUTS</span></span>

### <span data-ttu-id="8a2ee-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8a2ee-127">System.String</span></span>

## <span data-ttu-id="8a2ee-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a2ee-128">OUTPUTS</span></span>

### <span data-ttu-id="8a2ee-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="8a2ee-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="8a2ee-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a2ee-130">NOTES</span></span>

## <span data-ttu-id="8a2ee-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a2ee-131">RELATED LINKS</span></span>

<span data-ttu-id="8a2ee-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Nowe — AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="8a2ee-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
