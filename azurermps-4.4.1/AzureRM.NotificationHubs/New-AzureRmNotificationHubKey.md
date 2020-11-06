---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 419dd6efcf9152c03d3f94f5ab9ead06c3c234ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546172"
---
# <span data-ttu-id="c6525-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="c6525-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="c6525-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6525-102">SYNOPSIS</span></span>
<span data-ttu-id="c6525-103">Ponowne generowanie klucza reguły autoryzacji dla NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="c6525-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6525-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6525-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6525-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6525-105">DESCRIPTION</span></span>
<span data-ttu-id="c6525-106">Polecenie cmdlet New-AzureRmNotificationHubKey ponownie generuje klucz podstawowy/klucz pomocniczy reguły autoryzacji NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="c6525-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="c6525-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6525-107">EXAMPLES</span></span>

### <span data-ttu-id="c6525-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6525-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c6525-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="c6525-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c6525-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6525-110">PARAMETERS</span></span>

### <span data-ttu-id="c6525-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c6525-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="c6525-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c6525-112">-Force</span></span>
<span data-ttu-id="c6525-113">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6525-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c6525-114">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6525-114">-Namespace</span></span>
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

### <span data-ttu-id="c6525-115">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c6525-115">-NotificationHub</span></span>
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

### <span data-ttu-id="c6525-116">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c6525-116">-PolicyKey</span></span>
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

### <span data-ttu-id="c6525-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c6525-117">-ResourceGroup</span></span>
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

### <span data-ttu-id="c6525-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6525-118">-Confirm</span></span>
<span data-ttu-id="c6525-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6525-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6525-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6525-120">-WhatIf</span></span>
<span data-ttu-id="c6525-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6525-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6525-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6525-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6525-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6525-123">-DefaultProfile</span></span>
<span data-ttu-id="c6525-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6525-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6525-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6525-125">CommonParameters</span></span>
<span data-ttu-id="c6525-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6525-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6525-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6525-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6525-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6525-128">INPUTS</span></span>

## <span data-ttu-id="c6525-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6525-129">OUTPUTS</span></span>

### <span data-ttu-id="c6525-130">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c6525-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c6525-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6525-131">NOTES</span></span>

## <span data-ttu-id="c6525-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6525-132">RELATED LINKS</span></span>

