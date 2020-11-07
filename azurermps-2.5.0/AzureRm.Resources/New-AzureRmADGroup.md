---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898641"
---
# <span data-ttu-id="5a11a-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="5a11a-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="5a11a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a11a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a11a-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a11a-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a11a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a11a-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a11a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a11a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a11a-106">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a11a-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="5a11a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a11a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a11a-108">Przykład 1 — Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="5a11a-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="5a11a-109">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i pseudonimie poczty " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="5a11a-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="5a11a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a11a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a11a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a11a-111">-DefaultProfile</span></span>
<span data-ttu-id="5a11a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a11a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a11a-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a11a-113">-DisplayName</span></span>
<span data-ttu-id="5a11a-114">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="5a11a-114">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a11a-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="5a11a-115">-MailNickname</span></span>
<span data-ttu-id="5a11a-116">Pseudonim poczty grupy.</span><span class="sxs-lookup"><span data-stu-id="5a11a-116">The mail nickname for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a11a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a11a-117">-Confirm</span></span>
<span data-ttu-id="5a11a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a11a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a11a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a11a-119">-WhatIf</span></span>
<span data-ttu-id="5a11a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a11a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a11a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a11a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a11a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a11a-122">CommonParameters</span></span>
<span data-ttu-id="5a11a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a11a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a11a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a11a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a11a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a11a-125">INPUTS</span></span>

### <span data-ttu-id="5a11a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5a11a-126">System.String</span></span>

## <span data-ttu-id="5a11a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a11a-127">OUTPUTS</span></span>

### <span data-ttu-id="5a11a-128">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5a11a-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5a11a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a11a-129">NOTES</span></span>

## <span data-ttu-id="5a11a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a11a-130">RELATED LINKS</span></span>
