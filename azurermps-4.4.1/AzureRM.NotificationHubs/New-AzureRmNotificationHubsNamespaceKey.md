---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: ba33dd46a899f03539c39e61368570fb2bce0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543159"
---
# <span data-ttu-id="23f54-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="23f54-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="23f54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23f54-102">SYNOPSIS</span></span>
<span data-ttu-id="23f54-103">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="23f54-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23f54-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23f54-105">DESCRIPTION</span></span>
<span data-ttu-id="23f54-106">Polecenie cmdlet New-AzureRmNotificationHubNamespaceKey generuje ponownie klucz podstawowy/klucz pomocniczy reguły autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="23f54-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="23f54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23f54-107">EXAMPLES</span></span>

### <span data-ttu-id="23f54-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23f54-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="23f54-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="23f54-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="23f54-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23f54-110">PARAMETERS</span></span>

### <span data-ttu-id="23f54-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23f54-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="23f54-112">-Force</span><span class="sxs-lookup"><span data-stu-id="23f54-112">-Force</span></span>
<span data-ttu-id="23f54-113">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23f54-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="23f54-114">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23f54-114">-Namespace</span></span>
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

### <span data-ttu-id="23f54-115">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="23f54-115">-PolicyKey</span></span>
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

### <span data-ttu-id="23f54-116">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="23f54-116">-ResourceGroup</span></span>
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

### <span data-ttu-id="23f54-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23f54-117">-Confirm</span></span>
<span data-ttu-id="23f54-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f54-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f54-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f54-119">-WhatIf</span></span>
<span data-ttu-id="23f54-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f54-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f54-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23f54-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f54-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f54-122">-DefaultProfile</span></span>
<span data-ttu-id="23f54-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23f54-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f54-124">CommonParameters</span></span>
<span data-ttu-id="23f54-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f54-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f54-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23f54-127">INPUTS</span></span>

## <span data-ttu-id="23f54-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23f54-128">OUTPUTS</span></span>

### <span data-ttu-id="23f54-129">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="23f54-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="23f54-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23f54-130">NOTES</span></span>

## <span data-ttu-id="23f54-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23f54-131">RELATED LINKS</span></span>

