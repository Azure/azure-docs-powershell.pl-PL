---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: d1a5057b25c08d1c93512ad3f439a9b4b208552f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871816"
---
# <span data-ttu-id="7ba83-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="7ba83-101">New-AzADGroup</span></span>

## <span data-ttu-id="7ba83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ba83-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba83-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba83-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="7ba83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ba83-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <string>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba83-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ba83-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba83-106">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba83-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="7ba83-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ba83-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba83-108">Przykład 1 — Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="7ba83-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="7ba83-109">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i pseudonimie poczty "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="7ba83-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="7ba83-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ba83-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba83-111">-DefaultProfile</span></span>
<span data-ttu-id="7ba83-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba83-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba83-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="7ba83-113">-Description</span></span>
<span data-ttu-id="7ba83-114">Opis grupy.</span><span class="sxs-lookup"><span data-stu-id="7ba83-114">The description for the group.</span></span>

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

### <span data-ttu-id="7ba83-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7ba83-115">-DisplayName</span></span>
<span data-ttu-id="7ba83-116">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="7ba83-116">The display name for the group.</span></span>

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

### <span data-ttu-id="7ba83-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="7ba83-117">-MailNickname</span></span>
<span data-ttu-id="7ba83-118">Pseudonim poczty grupy.</span><span class="sxs-lookup"><span data-stu-id="7ba83-118">The mail nickname for the group.</span></span> <span data-ttu-id="7ba83-119">Nie może zawierać znaku @.</span><span class="sxs-lookup"><span data-stu-id="7ba83-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="7ba83-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ba83-120">-Confirm</span></span>
<span data-ttu-id="7ba83-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba83-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba83-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba83-122">-WhatIf</span></span>
<span data-ttu-id="7ba83-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba83-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba83-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ba83-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba83-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba83-125">CommonParameters</span></span>
<span data-ttu-id="7ba83-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba83-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba83-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba83-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba83-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ba83-128">INPUTS</span></span>

### <span data-ttu-id="7ba83-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba83-129">System.String</span></span>

## <span data-ttu-id="7ba83-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ba83-130">OUTPUTS</span></span>

### <span data-ttu-id="7ba83-131">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="7ba83-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="7ba83-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ba83-132">NOTES</span></span>

## <span data-ttu-id="7ba83-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ba83-133">RELATED LINKS</span></span>
