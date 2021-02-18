---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193227"
---
# <span data-ttu-id="1800b-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="1800b-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="1800b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1800b-102">SYNOPSIS</span></span>
<span data-ttu-id="1800b-103">Ponownie wygeneruj klucz reguły autoryzacji dla usługi NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="1800b-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="1800b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1800b-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1800b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1800b-105">DESCRIPTION</span></span>
<span data-ttu-id="1800b-106">New-AzNotificationHubKey polecenie cmdlet ponownie generuje klucz podstawowy/klucz pomocniczy reguły autoryzacji w witrynie NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="1800b-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="1800b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1800b-107">EXAMPLES</span></span>

### <span data-ttu-id="1800b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1800b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1800b-109">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="1800b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1800b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1800b-110">PARAMETERS</span></span>

### <span data-ttu-id="1800b-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1800b-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1800b-112">-DefaultProfile</span></span>
<span data-ttu-id="1800b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1800b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1800b-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1800b-114">-Force</span></span>
<span data-ttu-id="1800b-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1800b-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-116">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="1800b-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-117">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="1800b-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="1800b-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1800b-119">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1800b-120">-Confirm</span></span>
<span data-ttu-id="1800b-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1800b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1800b-122">-WhatIf</span></span>
<span data-ttu-id="1800b-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1800b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1800b-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1800b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1800b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1800b-125">CommonParameters</span></span>
<span data-ttu-id="1800b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1800b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1800b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1800b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1800b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1800b-128">INPUTS</span></span>

### <span data-ttu-id="1800b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1800b-129">System.String</span></span>

## <span data-ttu-id="1800b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1800b-130">OUTPUTS</span></span>

### <span data-ttu-id="1800b-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="1800b-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="1800b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1800b-132">NOTES</span></span>

## <span data-ttu-id="1800b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1800b-133">RELATED LINKS</span></span>
