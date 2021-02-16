---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186451"
---
# <span data-ttu-id="8ccf2-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="8ccf2-101">New-AzADGroup</span></span>

## <span data-ttu-id="8ccf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ccf2-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccf2-103">Tworzy nową grupę usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="8ccf2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ccf2-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ccf2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ccf2-105">DESCRIPTION</span></span>
<span data-ttu-id="8ccf2-106">Tworzy nową grupę usługi Active Directory. Poniżej przedstawiono wymagane uprawnienia:</span><span class="sxs-lookup"><span data-stu-id="8ccf2-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="8ccf2-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="8ccf2-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="8ccf2-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ccf2-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="8ccf2-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8ccf2-109">Microsoft Graph</span></span>
  - <span data-ttu-id="8ccf2-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ccf2-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="8ccf2-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="8ccf2-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="8ccf2-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ccf2-112">EXAMPLES</span></span>

### <span data-ttu-id="8ccf2-113">Przykład 1. Tworzenie nowej grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="8ccf2-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="8ccf2-114">Tworzy nową grupę usługi AD o nazwie "MyGroupDisplayName" i nazwie poczty "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="8ccf2-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="8ccf2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ccf2-115">PARAMETERS</span></span>

### <span data-ttu-id="8ccf2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccf2-116">-DefaultProfile</span></span>
<span data-ttu-id="8ccf2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ccf2-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="8ccf2-118">-Description</span></span>
<span data-ttu-id="8ccf2-119">Opis grupy.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-119">The description for the group.</span></span>

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

### <span data-ttu-id="8ccf2-120">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ccf2-120">-DisplayName</span></span>
<span data-ttu-id="8ccf2-121">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-121">The display name for the group.</span></span>

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

### <span data-ttu-id="8ccf2-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="8ccf2-122">-MailNickname</span></span>
<span data-ttu-id="8ccf2-123">Nick pocztowy grupy.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-123">The mail nickname for the group.</span></span> <span data-ttu-id="8ccf2-124">Nie może zawierać znaku @.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="8ccf2-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ccf2-125">-Confirm</span></span>
<span data-ttu-id="8ccf2-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ccf2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ccf2-127">-WhatIf</span></span>
<span data-ttu-id="8ccf2-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ccf2-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ccf2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccf2-130">CommonParameters</span></span>
<span data-ttu-id="8ccf2-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccf2-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ccf2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccf2-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ccf2-133">INPUTS</span></span>

### <span data-ttu-id="8ccf2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8ccf2-134">System.String</span></span>

## <span data-ttu-id="8ccf2-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ccf2-135">OUTPUTS</span></span>

### <span data-ttu-id="8ccf2-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8ccf2-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8ccf2-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ccf2-137">NOTES</span></span>

## <span data-ttu-id="8ccf2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ccf2-138">RELATED LINKS</span></span>
