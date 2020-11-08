---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051748"
---
# <span data-ttu-id="e42e8-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="e42e8-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="e42e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e42e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e42e8-103">Ponowne generowanie klucza reguły autoryzacji dla NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="e42e8-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="e42e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e42e8-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e42e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e42e8-105">DESCRIPTION</span></span>
<span data-ttu-id="e42e8-106">Polecenie cmdlet New-AzNotificationHubKey ponownie generuje klucz podstawowy/klucz pomocniczy reguły autoryzacji NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="e42e8-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="e42e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e42e8-107">EXAMPLES</span></span>

### <span data-ttu-id="e42e8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e42e8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e42e8-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="e42e8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e42e8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e42e8-110">PARAMETERS</span></span>

### <span data-ttu-id="e42e8-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e42e8-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="e42e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42e8-112">-DefaultProfile</span></span>
<span data-ttu-id="e42e8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e42e8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e42e8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e42e8-114">-Force</span></span>
<span data-ttu-id="e42e8-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e42e8-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e42e8-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e42e8-116">-Namespace</span></span>
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

### <span data-ttu-id="e42e8-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e42e8-117">-NotificationHub</span></span>
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

### <span data-ttu-id="e42e8-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="e42e8-118">-PolicyKey</span></span>
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

### <span data-ttu-id="e42e8-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e42e8-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="e42e8-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e42e8-120">-Confirm</span></span>
<span data-ttu-id="e42e8-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42e8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42e8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42e8-122">-WhatIf</span></span>
<span data-ttu-id="e42e8-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42e8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42e8-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e42e8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42e8-125">CommonParameters</span></span>
<span data-ttu-id="e42e8-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42e8-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42e8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42e8-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42e8-128">INPUTS</span></span>

### <span data-ttu-id="e42e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e42e8-129">System.String</span></span>

## <span data-ttu-id="e42e8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e42e8-130">OUTPUTS</span></span>

### <span data-ttu-id="e42e8-131">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="e42e8-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="e42e8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e42e8-132">NOTES</span></span>

## <span data-ttu-id="e42e8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e42e8-133">RELATED LINKS</span></span>
