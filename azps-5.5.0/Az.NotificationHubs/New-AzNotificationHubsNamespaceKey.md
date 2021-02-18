---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240482"
---
# <span data-ttu-id="c7f79-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c7f79-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="c7f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f79-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f79-103">Ponownie wygeneruj klucz reguły autoryzacji dla przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c7f79-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="c7f79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c7f79-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f79-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c7f79-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f79-106">New-AzNotificationHubNamespaceKey cmdlet ponownie generuje klucz podstawowy/klucz pomocniczy reguły autoryzacji przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c7f79-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="c7f79-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c7f79-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f79-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7f79-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c7f79-109">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="c7f79-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c7f79-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7f79-110">PARAMETERS</span></span>

### <span data-ttu-id="c7f79-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7f79-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f79-112">-DefaultProfile</span></span>
<span data-ttu-id="c7f79-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c7f79-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7f79-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c7f79-114">-Force</span></span>
<span data-ttu-id="c7f79-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c7f79-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c7f79-116">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c7f79-116">-Namespace</span></span>
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

### <span data-ttu-id="c7f79-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c7f79-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f79-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7f79-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="c7f79-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7f79-119">-Confirm</span></span>
<span data-ttu-id="c7f79-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c7f79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f79-121">-WhatIf</span></span>
<span data-ttu-id="c7f79-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7f79-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f79-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c7f79-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f79-124">CommonParameters</span></span>
<span data-ttu-id="c7f79-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f79-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f79-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7f79-127">INPUTS</span></span>

### <span data-ttu-id="c7f79-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c7f79-128">System.String</span></span>

## <span data-ttu-id="c7f79-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7f79-129">OUTPUTS</span></span>

### <span data-ttu-id="c7f79-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c7f79-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c7f79-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c7f79-131">NOTES</span></span>

## <span data-ttu-id="c7f79-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7f79-132">RELATED LINKS</span></span>
