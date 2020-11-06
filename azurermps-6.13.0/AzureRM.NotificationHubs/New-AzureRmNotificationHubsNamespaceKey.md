---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 070befe362c6730b3592eac18cf8db70cd688716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544991"
---
# <span data-ttu-id="a4fcf-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="a4fcf-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="a4fcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fcf-103">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4fcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4fcf-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fcf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="a4fcf-106">Polecenie cmdlet New-AzureRmNotificationHubNamespaceKey generuje ponownie klucz podstawowy/klucz pomocniczy reguły autoryzacji obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="a4fcf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="a4fcf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4fcf-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a4fcf-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="a4fcf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a4fcf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4fcf-110">PARAMETERS</span></span>

### <span data-ttu-id="a4fcf-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4fcf-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="a4fcf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fcf-112">-DefaultProfile</span></span>
<span data-ttu-id="a4fcf-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4fcf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4fcf-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a4fcf-114">-Force</span></span>
<span data-ttu-id="a4fcf-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a4fcf-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4fcf-116">-Namespace</span></span>
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

### <span data-ttu-id="a4fcf-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="a4fcf-117">-PolicyKey</span></span>
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

### <span data-ttu-id="a4fcf-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4fcf-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="a4fcf-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4fcf-119">-Confirm</span></span>
<span data-ttu-id="a4fcf-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fcf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fcf-121">-WhatIf</span></span>
<span data-ttu-id="a4fcf-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fcf-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fcf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fcf-124">CommonParameters</span></span>
<span data-ttu-id="a4fcf-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fcf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fcf-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fcf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fcf-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4fcf-127">INPUTS</span></span>

### <span data-ttu-id="a4fcf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fcf-128">System.String</span></span>

## <span data-ttu-id="a4fcf-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4fcf-129">OUTPUTS</span></span>

### <span data-ttu-id="a4fcf-130">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="a4fcf-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="a4fcf-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4fcf-131">NOTES</span></span>

## <span data-ttu-id="a4fcf-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4fcf-132">RELATED LINKS</span></span>
