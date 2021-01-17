---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336202"
---
# <span data-ttu-id="6bf6f-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6bf6f-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="6bf6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bf6f-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf6f-103">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="6bf6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bf6f-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bf6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6bf6f-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf6f-106">Polecenie cmdlet New-AzNotificationHubNamespaceKey generuje ponownie klucz podstawowy/klucz pomocniczy reguły autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="6bf6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bf6f-107">EXAMPLES</span></span>

### <span data-ttu-id="6bf6f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bf6f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6bf6f-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="6bf6f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6bf6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bf6f-110">PARAMETERS</span></span>

### <span data-ttu-id="6bf6f-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6bf6f-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="6bf6f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf6f-112">-DefaultProfile</span></span>
<span data-ttu-id="6bf6f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6bf6f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bf6f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6bf6f-114">-Force</span></span>
<span data-ttu-id="6bf6f-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6bf6f-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6bf6f-116">-Namespace</span></span>
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

### <span data-ttu-id="6bf6f-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="6bf6f-117">-PolicyKey</span></span>
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

### <span data-ttu-id="6bf6f-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6bf6f-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="6bf6f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bf6f-119">-Confirm</span></span>
<span data-ttu-id="6bf6f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf6f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf6f-121">-WhatIf</span></span>
<span data-ttu-id="6bf6f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf6f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf6f-124">CommonParameters</span></span>
<span data-ttu-id="6bf6f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf6f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf6f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf6f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bf6f-127">INPUTS</span></span>

### <span data-ttu-id="6bf6f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6bf6f-128">System.String</span></span>

## <span data-ttu-id="6bf6f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bf6f-129">OUTPUTS</span></span>

### <span data-ttu-id="6bf6f-130">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6bf6f-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6bf6f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bf6f-131">NOTES</span></span>

## <span data-ttu-id="6bf6f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bf6f-132">RELATED LINKS</span></span>
