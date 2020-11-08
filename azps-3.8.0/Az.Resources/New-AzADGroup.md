---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053425"
---
# <span data-ttu-id="9cbec-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="9cbec-101">New-AzADGroup</span></span>

## <span data-ttu-id="9cbec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cbec-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbec-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9cbec-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="9cbec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cbec-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cbec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cbec-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbec-106">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9cbec-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="9cbec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cbec-107">EXAMPLES</span></span>

### <span data-ttu-id="9cbec-108">Przykład 1 — Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="9cbec-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="9cbec-109">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i pseudonimie poczty "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="9cbec-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="9cbec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cbec-110">PARAMETERS</span></span>

### <span data-ttu-id="9cbec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbec-111">-DefaultProfile</span></span>
<span data-ttu-id="9cbec-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbec-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="9cbec-113">-Description</span></span>
<span data-ttu-id="9cbec-114">Opis grupy.</span><span class="sxs-lookup"><span data-stu-id="9cbec-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbec-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9cbec-115">-DisplayName</span></span>
<span data-ttu-id="9cbec-116">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="9cbec-116">The display name for the group.</span></span>

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

### <span data-ttu-id="9cbec-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="9cbec-117">-MailNickname</span></span>
<span data-ttu-id="9cbec-118">Pseudonim poczty grupy.</span><span class="sxs-lookup"><span data-stu-id="9cbec-118">The mail nickname for the group.</span></span> <span data-ttu-id="9cbec-119">Nie może zawierać znaku @.</span><span class="sxs-lookup"><span data-stu-id="9cbec-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="9cbec-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cbec-120">-Confirm</span></span>
<span data-ttu-id="9cbec-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cbec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbec-122">-WhatIf</span></span>
<span data-ttu-id="9cbec-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cbec-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cbec-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9cbec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbec-125">CommonParameters</span></span>
<span data-ttu-id="9cbec-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbec-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cbec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbec-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cbec-128">INPUTS</span></span>

### <span data-ttu-id="9cbec-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbec-129">System.String</span></span>

## <span data-ttu-id="9cbec-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cbec-130">OUTPUTS</span></span>

### <span data-ttu-id="9cbec-131">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9cbec-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9cbec-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cbec-132">NOTES</span></span>

## <span data-ttu-id="9cbec-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cbec-133">RELATED LINKS</span></span>
