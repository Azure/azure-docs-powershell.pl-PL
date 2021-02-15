---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 48ddcf7c6bed9e31bec486eaaa433c35eaed0fe3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399026"
---
# <span data-ttu-id="d9407-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d9407-101">New-AzActionGroup</span></span>

## <span data-ttu-id="d9407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9407-102">SYNOPSIS</span></span>
<span data-ttu-id="d9407-103">Tworzy obiekt odwołania ActionGroup w pamięci.</span><span class="sxs-lookup"><span data-stu-id="d9407-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="d9407-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9407-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9407-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9407-105">DESCRIPTION</span></span>
<span data-ttu-id="d9407-106">Polecenie **cmdlet New-AzActionGroup** tworzy w pamięci obiekt odwołania do grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="d9407-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="d9407-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9407-107">EXAMPLES</span></span>

### <span data-ttu-id="d9407-108">Przykład 1. Tworzenie w pamięci obiektu odwołania do grupy akcji</span><span class="sxs-lookup"><span data-stu-id="d9407-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="d9407-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9407-109">PARAMETERS</span></span>

### <span data-ttu-id="d9407-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="d9407-110">-ActionGroupId</span></span>
<span data-ttu-id="d9407-111">Identyfikator/nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="d9407-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="d9407-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9407-112">-DefaultProfile</span></span>
<span data-ttu-id="d9407-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d9407-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9407-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="d9407-114">-WebhookProperty</span></span>
<span data-ttu-id="d9407-115">Właściwości sieci Web grupy akcji</span><span class="sxs-lookup"><span data-stu-id="d9407-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="d9407-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9407-116">CommonParameters</span></span>
<span data-ttu-id="d9407-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9407-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9407-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9407-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9407-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9407-119">INPUTS</span></span>

### <span data-ttu-id="d9407-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d9407-120">System.String</span></span>

### <span data-ttu-id="d9407-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9407-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d9407-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9407-122">OUTPUTS</span></span>

### <span data-ttu-id="d9407-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="d9407-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="d9407-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9407-124">NOTES</span></span>

## <span data-ttu-id="d9407-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9407-125">RELATED LINKS</span></span>

[<span data-ttu-id="d9407-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9407-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d9407-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9407-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="d9407-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9407-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="d9407-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9407-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="d9407-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d9407-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



