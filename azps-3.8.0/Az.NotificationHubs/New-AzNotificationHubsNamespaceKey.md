---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051747"
---
# <span data-ttu-id="af823-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="af823-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="af823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af823-102">SYNOPSIS</span></span>
<span data-ttu-id="af823-103">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="af823-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="af823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af823-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af823-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af823-105">DESCRIPTION</span></span>
<span data-ttu-id="af823-106">Polecenie cmdlet New-AzNotificationHubNamespaceKey generuje ponownie klucz podstawowy/klucz pomocniczy reguły autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="af823-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="af823-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af823-107">EXAMPLES</span></span>

### <span data-ttu-id="af823-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af823-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="af823-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="af823-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="af823-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af823-110">PARAMETERS</span></span>

### <span data-ttu-id="af823-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="af823-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="af823-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af823-112">-DefaultProfile</span></span>
<span data-ttu-id="af823-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="af823-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af823-114">-Force</span><span class="sxs-lookup"><span data-stu-id="af823-114">-Force</span></span>
<span data-ttu-id="af823-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af823-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af823-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="af823-116">-Namespace</span></span>
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

### <span data-ttu-id="af823-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="af823-117">-PolicyKey</span></span>
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

### <span data-ttu-id="af823-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="af823-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="af823-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af823-119">-Confirm</span></span>
<span data-ttu-id="af823-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af823-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af823-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af823-121">-WhatIf</span></span>
<span data-ttu-id="af823-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af823-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af823-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af823-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af823-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af823-124">CommonParameters</span></span>
<span data-ttu-id="af823-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af823-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af823-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af823-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af823-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af823-127">INPUTS</span></span>

### <span data-ttu-id="af823-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af823-128">System.String</span></span>

## <span data-ttu-id="af823-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af823-129">OUTPUTS</span></span>

### <span data-ttu-id="af823-130">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="af823-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="af823-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af823-131">NOTES</span></span>

## <span data-ttu-id="af823-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af823-132">RELATED LINKS</span></span>
