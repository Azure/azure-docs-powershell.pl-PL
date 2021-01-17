---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361552"
---
# <span data-ttu-id="46774-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="46774-101">New-AzActionGroup</span></span>

## <span data-ttu-id="46774-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46774-102">SYNOPSIS</span></span>
<span data-ttu-id="46774-103">Tworzy obiekt odwołania do obiektu Actions w pamięci.</span><span class="sxs-lookup"><span data-stu-id="46774-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="46774-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46774-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46774-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46774-105">DESCRIPTION</span></span>
<span data-ttu-id="46774-106">Polecenie cmdlet **New-AzActionGroup** tworzy obiekt odwołania do grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="46774-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="46774-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46774-107">EXAMPLES</span></span>

### <span data-ttu-id="46774-108">Przykład 1: Tworzenie obiektu odwołania do grupy akcji w pamięci</span><span class="sxs-lookup"><span data-stu-id="46774-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="46774-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46774-109">PARAMETERS</span></span>

### <span data-ttu-id="46774-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="46774-110">-ActionGroupId</span></span>
<span data-ttu-id="46774-111">Identyfikator/nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="46774-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="46774-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46774-112">-DefaultProfile</span></span>
<span data-ttu-id="46774-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="46774-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46774-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="46774-114">-WebhookProperty</span></span>
<span data-ttu-id="46774-115">Właściwości elementu webhook grupy Actions</span><span class="sxs-lookup"><span data-stu-id="46774-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="46774-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46774-116">CommonParameters</span></span>
<span data-ttu-id="46774-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46774-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46774-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46774-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46774-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46774-119">INPUTS</span></span>

### <span data-ttu-id="46774-120">System. String</span><span class="sxs-lookup"><span data-stu-id="46774-120">System.String</span></span>

### <span data-ttu-id="46774-121">System. Collections. Generic. dictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="46774-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="46774-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46774-122">OUTPUTS</span></span>

### <span data-ttu-id="46774-123">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="46774-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="46774-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46774-124">NOTES</span></span>

## <span data-ttu-id="46774-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46774-125">RELATED LINKS</span></span>

[<span data-ttu-id="46774-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="46774-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="46774-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="46774-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="46774-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="46774-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="46774-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="46774-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="46774-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="46774-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="46774-131">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="46774-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

