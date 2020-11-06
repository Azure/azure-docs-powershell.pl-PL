---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552851"
---
# <span data-ttu-id="88d23-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="88d23-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="88d23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88d23-102">SYNOPSIS</span></span>
<span data-ttu-id="88d23-103">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="88d23-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88d23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88d23-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88d23-105">DESCRIPTION</span></span>
<span data-ttu-id="88d23-106">Polecenie cmdlet New-AzureRmNotificationHubNamespaceKey generuje ponownie klucz podstawowy/klucz pomocniczy reguły autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="88d23-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="88d23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88d23-107">EXAMPLES</span></span>

### <span data-ttu-id="88d23-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88d23-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="88d23-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="88d23-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="88d23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88d23-110">PARAMETERS</span></span>

### <span data-ttu-id="88d23-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88d23-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d23-112">-DefaultProfile</span></span>
<span data-ttu-id="88d23-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="88d23-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-114">-Force</span><span class="sxs-lookup"><span data-stu-id="88d23-114">-Force</span></span>
<span data-ttu-id="88d23-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88d23-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88d23-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="88d23-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="88d23-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88d23-119">-Confirm</span></span>
<span data-ttu-id="88d23-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88d23-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d23-121">-WhatIf</span></span>
<span data-ttu-id="88d23-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88d23-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d23-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88d23-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d23-124">CommonParameters</span></span>
<span data-ttu-id="88d23-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d23-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d23-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88d23-127">INPUTS</span></span>

### <span data-ttu-id="88d23-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88d23-128">None</span></span>
<span data-ttu-id="88d23-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="88d23-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88d23-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88d23-130">OUTPUTS</span></span>

### <span data-ttu-id="88d23-131">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="88d23-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="88d23-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88d23-132">NOTES</span></span>

## <span data-ttu-id="88d23-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88d23-133">RELATED LINKS</span></span>

