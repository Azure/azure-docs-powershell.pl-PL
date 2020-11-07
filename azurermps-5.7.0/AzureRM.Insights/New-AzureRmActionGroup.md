---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717114"
---
# <span data-ttu-id="6157d-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6157d-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="6157d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6157d-102">SYNOPSIS</span></span>
<span data-ttu-id="6157d-103">Tworzy obiekt odwołania do obiektu Actions w pamięci.</span><span class="sxs-lookup"><span data-stu-id="6157d-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6157d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6157d-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6157d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6157d-105">DESCRIPTION</span></span>
<span data-ttu-id="6157d-106">Polecenie cmdlet **New-AzureRmActionGroup** tworzy obiekt odwołania do grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="6157d-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="6157d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6157d-107">EXAMPLES</span></span>

### <span data-ttu-id="6157d-108">Przykład 1: Tworzenie obiektu odwołania do grupy akcji w pamięci</span><span class="sxs-lookup"><span data-stu-id="6157d-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="6157d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6157d-109">PARAMETERS</span></span>

### <span data-ttu-id="6157d-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="6157d-110">-ActionGroupId</span></span>
<span data-ttu-id="6157d-111">Identyfikator/nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="6157d-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6157d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6157d-112">-DefaultProfile</span></span>
<span data-ttu-id="6157d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6157d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6157d-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="6157d-114">-WebhookProperty</span></span>
<span data-ttu-id="6157d-115">Właściwości elementu webhook grupy Actions</span><span class="sxs-lookup"><span data-stu-id="6157d-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6157d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6157d-116">CommonParameters</span></span>
<span data-ttu-id="6157d-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6157d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6157d-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6157d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6157d-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6157d-119">INPUTS</span></span>

### <span data-ttu-id="6157d-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6157d-120">None</span></span>
<span data-ttu-id="6157d-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6157d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6157d-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6157d-122">OUTPUTS</span></span>

### <span data-ttu-id="6157d-123">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="6157d-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="6157d-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6157d-124">NOTES</span></span>

## <span data-ttu-id="6157d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6157d-125">RELATED LINKS</span></span>

[<span data-ttu-id="6157d-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6157d-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6157d-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6157d-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6157d-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6157d-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6157d-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6157d-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6157d-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6157d-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6157d-131">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6157d-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

