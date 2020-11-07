---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: f426dc06d08e10d0811382b00e2072f65ebf1b0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708868"
---
# <span data-ttu-id="c0603-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="c0603-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="c0603-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0603-102">SYNOPSIS</span></span>
<span data-ttu-id="c0603-103">Ponowne generowanie klucza reguły autoryzacji dla NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="c0603-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="c0603-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0603-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0603-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0603-105">DESCRIPTION</span></span>
<span data-ttu-id="c0603-106">Polecenie cmdlet New-AzNotificationHubKey ponownie generuje klucz podstawowy/klucz pomocniczy reguły autoryzacji NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="c0603-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="c0603-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0603-107">EXAMPLES</span></span>

### <span data-ttu-id="c0603-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0603-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c0603-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="c0603-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c0603-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0603-110">PARAMETERS</span></span>

### <span data-ttu-id="c0603-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0603-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="c0603-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0603-112">-DefaultProfile</span></span>
<span data-ttu-id="c0603-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0603-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0603-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c0603-114">-Force</span></span>
<span data-ttu-id="c0603-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0603-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c0603-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c0603-116">-Namespace</span></span>
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

### <span data-ttu-id="c0603-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c0603-117">-NotificationHub</span></span>
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

### <span data-ttu-id="c0603-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c0603-118">-PolicyKey</span></span>
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

### <span data-ttu-id="c0603-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c0603-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="c0603-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0603-120">-Confirm</span></span>
<span data-ttu-id="c0603-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0603-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0603-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0603-122">-WhatIf</span></span>
<span data-ttu-id="c0603-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0603-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0603-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0603-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0603-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0603-125">CommonParameters</span></span>
<span data-ttu-id="c0603-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0603-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0603-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0603-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0603-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0603-128">INPUTS</span></span>

### <span data-ttu-id="c0603-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c0603-129">System.String</span></span>

## <span data-ttu-id="c0603-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0603-130">OUTPUTS</span></span>

### <span data-ttu-id="c0603-131">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c0603-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c0603-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0603-132">NOTES</span></span>

## <span data-ttu-id="c0603-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0603-133">RELATED LINKS</span></span>
