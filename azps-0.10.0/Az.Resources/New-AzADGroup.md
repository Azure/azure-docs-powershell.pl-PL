---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892538"
---
# <span data-ttu-id="5502f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="5502f-101">New-AzADGroup</span></span>

## <span data-ttu-id="5502f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5502f-102">SYNOPSIS</span></span>
<span data-ttu-id="5502f-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5502f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="5502f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5502f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5502f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5502f-105">DESCRIPTION</span></span>
<span data-ttu-id="5502f-106">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5502f-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="5502f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5502f-107">EXAMPLES</span></span>

### <span data-ttu-id="5502f-108">Przykład 1 — Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="5502f-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="5502f-109">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i pseudonimie poczty " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="5502f-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="5502f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5502f-110">PARAMETERS</span></span>

### <span data-ttu-id="5502f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5502f-111">-DefaultProfile</span></span>
<span data-ttu-id="5502f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5502f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5502f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5502f-113">-DisplayName</span></span>
<span data-ttu-id="5502f-114">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="5502f-114">The display name for the group.</span></span>

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

### <span data-ttu-id="5502f-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="5502f-115">-MailNickname</span></span>
<span data-ttu-id="5502f-116">Pseudonim poczty grupy.</span><span class="sxs-lookup"><span data-stu-id="5502f-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="5502f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5502f-117">-Confirm</span></span>
<span data-ttu-id="5502f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5502f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5502f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5502f-119">-WhatIf</span></span>
<span data-ttu-id="5502f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5502f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5502f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5502f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5502f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5502f-122">CommonParameters</span></span>
<span data-ttu-id="5502f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5502f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5502f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5502f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5502f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5502f-125">INPUTS</span></span>

### <span data-ttu-id="5502f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5502f-126">System.String</span></span>

## <span data-ttu-id="5502f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5502f-127">OUTPUTS</span></span>

### <span data-ttu-id="5502f-128">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5502f-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5502f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5502f-129">NOTES</span></span>

## <span data-ttu-id="5502f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5502f-130">RELATED LINKS</span></span>
