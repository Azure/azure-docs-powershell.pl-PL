---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 8cf82f8ec01bc2a02470daf6dd0bd336bb564813
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867291"
---
# <span data-ttu-id="f32ba-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f32ba-101">New-AzActionGroup</span></span>

## <span data-ttu-id="f32ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f32ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f32ba-103">Tworzy obiekt odwołania do obiektu Actions w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f32ba-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="f32ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f32ba-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f32ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f32ba-105">DESCRIPTION</span></span>
<span data-ttu-id="f32ba-106">Polecenie cmdlet **New-AzActionGroup** tworzy obiekt odwołania do grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f32ba-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="f32ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f32ba-107">EXAMPLES</span></span>

### <span data-ttu-id="f32ba-108">Przykład 1: Tworzenie obiektu odwołania do grupy akcji w pamięci</span><span class="sxs-lookup"><span data-stu-id="f32ba-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="f32ba-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f32ba-109">PARAMETERS</span></span>

### <span data-ttu-id="f32ba-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="f32ba-110">-ActionGroupId</span></span>
<span data-ttu-id="f32ba-111">Identyfikator/nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="f32ba-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="f32ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32ba-112">-DefaultProfile</span></span>
<span data-ttu-id="f32ba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f32ba-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f32ba-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="f32ba-114">-WebhookProperty</span></span>
<span data-ttu-id="f32ba-115">Właściwości elementu webhook grupy Actions</span><span class="sxs-lookup"><span data-stu-id="f32ba-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="f32ba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32ba-116">CommonParameters</span></span>
<span data-ttu-id="f32ba-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32ba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32ba-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32ba-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32ba-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f32ba-119">INPUTS</span></span>

### <span data-ttu-id="f32ba-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f32ba-120">System.String</span></span>

### <span data-ttu-id="f32ba-121">System. Collections. Generic. dictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f32ba-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f32ba-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f32ba-122">OUTPUTS</span></span>

### <span data-ttu-id="f32ba-123">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="f32ba-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="f32ba-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f32ba-124">NOTES</span></span>

## <span data-ttu-id="f32ba-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f32ba-125">RELATED LINKS</span></span>

[<span data-ttu-id="f32ba-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f32ba-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f32ba-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f32ba-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="f32ba-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f32ba-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="f32ba-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f32ba-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="f32ba-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f32ba-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="f32ba-131">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f32ba-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
