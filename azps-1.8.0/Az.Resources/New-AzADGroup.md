---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708372"
---
# <span data-ttu-id="d8998-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="d8998-101">New-AzADGroup</span></span>

## <span data-ttu-id="d8998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8998-102">SYNOPSIS</span></span>
<span data-ttu-id="d8998-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8998-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="d8998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8998-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8998-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8998-105">DESCRIPTION</span></span>
<span data-ttu-id="d8998-106">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8998-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="d8998-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8998-107">EXAMPLES</span></span>

### <span data-ttu-id="d8998-108">Przykład 1 — Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="d8998-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="d8998-109">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i pseudonimie poczty "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="d8998-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="d8998-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8998-110">PARAMETERS</span></span>

### <span data-ttu-id="d8998-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8998-111">-DefaultProfile</span></span>
<span data-ttu-id="d8998-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8998-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8998-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8998-113">-DisplayName</span></span>
<span data-ttu-id="d8998-114">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="d8998-114">The display name for the group.</span></span>

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

### <span data-ttu-id="d8998-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="d8998-115">-MailNickname</span></span>
<span data-ttu-id="d8998-116">Pseudonim poczty grupy.</span><span class="sxs-lookup"><span data-stu-id="d8998-116">The mail nickname for the group.</span></span> <span data-ttu-id="d8998-117">Nie może zawierać znaku @.</span><span class="sxs-lookup"><span data-stu-id="d8998-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="d8998-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8998-118">-Confirm</span></span>
<span data-ttu-id="d8998-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8998-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8998-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8998-120">-WhatIf</span></span>
<span data-ttu-id="d8998-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8998-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8998-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8998-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8998-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8998-123">CommonParameters</span></span>
<span data-ttu-id="d8998-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8998-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8998-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8998-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8998-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8998-126">INPUTS</span></span>

### <span data-ttu-id="d8998-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d8998-127">System.String</span></span>

## <span data-ttu-id="d8998-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8998-128">OUTPUTS</span></span>

### <span data-ttu-id="d8998-129">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d8998-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="d8998-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8998-130">NOTES</span></span>

## <span data-ttu-id="d8998-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8998-131">RELATED LINKS</span></span>
