---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 213e488dde914a8e87b76d6c3765f5dbe99a527a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399978"
---
# <span data-ttu-id="f338d-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f338d-101">New-AzADUser</span></span>

## <span data-ttu-id="f338d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f338d-102">SYNOPSIS</span></span>
<span data-ttu-id="f338d-103">Tworzy nowego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f338d-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="f338d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f338d-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f338d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f338d-105">DESCRIPTION</span></span>
<span data-ttu-id="f338d-106">Tworzy nowego użytkownika usługi Active Directory (konto służbowe, które jest również popularne jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="f338d-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="f338d-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="f338d-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="f338d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f338d-108">EXAMPLES</span></span>

### <span data-ttu-id="f338d-109">Przykład 1. Tworzenie nowego użytkownika usługi AD</span><span class="sxs-lookup"><span data-stu-id="f338d-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="f338d-110">Tworzy nowego użytkownika usługi AD o nazwie "MyDisplayName" i głównej nazwie użytkownika myemail@domain.com " w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="f338d-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="f338d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f338d-111">PARAMETERS</span></span>

### <span data-ttu-id="f338d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f338d-112">-DefaultProfile</span></span>
<span data-ttu-id="f338d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f338d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f338d-114">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="f338d-114">-DisplayName</span></span>
<span data-ttu-id="f338d-115">Nazwa wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f338d-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="f338d-116">przykład "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="f338d-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="f338d-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="f338d-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="f338d-118">Należy określić, czy użytkownik musi zmienić hasło podczas następnego pomyślnego logowania (true).</span><span class="sxs-lookup"><span data-stu-id="f338d-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="f338d-119">Zachowaniem domyślnym jest (fałsz), aby nie zmieniać hasła podczas następnego pomyślnego logowania.</span><span class="sxs-lookup"><span data-stu-id="f338d-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f338d-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="f338d-120">-ImmutableId</span></span>
<span data-ttu-id="f338d-121">Należy ją określić tylko w przypadku używania domeny federskiej na potrzeby właściwości głównej nazwy użytkownika (upn).</span><span class="sxs-lookup"><span data-stu-id="f338d-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="f338d-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="f338d-122">-MailNickname</span></span>
<span data-ttu-id="f338d-123">Alias poczty dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f338d-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="f338d-124">— Hasło</span><span class="sxs-lookup"><span data-stu-id="f338d-124">-Password</span></span>
<span data-ttu-id="f338d-125">Hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f338d-125">Password for the user.</span></span>
<span data-ttu-id="f338d-126">Musi ona spełniać wymagania dotyczące złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f338d-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="f338d-127">Zalecane jest ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="f338d-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f338d-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f338d-128">-UserPrincipalName</span></span>
<span data-ttu-id="f338d-129">Główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f338d-129">The user principal name.</span></span>
<span data-ttu-id="f338d-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="f338d-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="f338d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f338d-131">-Confirm</span></span>
<span data-ttu-id="f338d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f338d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f338d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f338d-133">-WhatIf</span></span>
<span data-ttu-id="f338d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f338d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f338d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f338d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f338d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f338d-136">CommonParameters</span></span>
<span data-ttu-id="f338d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f338d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f338d-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f338d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f338d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f338d-139">INPUTS</span></span>

### <span data-ttu-id="f338d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f338d-140">System.String</span></span>

### <span data-ttu-id="f338d-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f338d-141">System.Security.SecureString</span></span>

### <span data-ttu-id="f338d-142">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f338d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f338d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f338d-143">OUTPUTS</span></span>

### <span data-ttu-id="f338d-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="f338d-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="f338d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f338d-145">NOTES</span></span>

## <span data-ttu-id="f338d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f338d-146">RELATED LINKS</span></span>

[<span data-ttu-id="f338d-147">Get-AzadUser</span><span class="sxs-lookup"><span data-stu-id="f338d-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="f338d-148">Remove-AzadUser</span><span class="sxs-lookup"><span data-stu-id="f338d-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
