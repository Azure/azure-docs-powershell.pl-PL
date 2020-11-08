---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: c7863e62330dc26d9733d21eb8e4d11753e06d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219935"
---
# <span data-ttu-id="27af3-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27af3-101">New-AzADUser</span></span>

## <span data-ttu-id="27af3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27af3-102">SYNOPSIS</span></span>
<span data-ttu-id="27af3-103">Tworzy nowego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="27af3-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="27af3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27af3-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27af3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="27af3-105">DESCRIPTION</span></span>
<span data-ttu-id="27af3-106">Tworzy nowego użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="27af3-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="27af3-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="27af3-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="27af3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27af3-108">EXAMPLES</span></span>

### <span data-ttu-id="27af3-109">Przykład 1. Tworzenie nowego użytkownika usługi AD</span><span class="sxs-lookup"><span data-stu-id="27af3-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="27af3-110">Tworzy nowego użytkownika usługi AD o nazwie "WebDisplayName" i głównej nazwie użytkownika " myemail@domain.com " w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="27af3-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="27af3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27af3-111">PARAMETERS</span></span>

### <span data-ttu-id="27af3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27af3-112">-DefaultProfile</span></span>
<span data-ttu-id="27af3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="27af3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27af3-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27af3-114">-DisplayName</span></span>
<span data-ttu-id="27af3-115">Nazwa wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27af3-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="27af3-116">przykład "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="27af3-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="27af3-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="27af3-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="27af3-118">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="27af3-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="27af3-119">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="27af3-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="27af3-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="27af3-120">-ImmutableId</span></span>
<span data-ttu-id="27af3-121">Należy ją określić tylko wtedy, gdy używana jest domena federacyjna dla właściwości głównej nazwy użytkownika (UPN) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27af3-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="27af3-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="27af3-122">-MailNickname</span></span>
<span data-ttu-id="27af3-123">Alias e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27af3-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="27af3-124">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="27af3-124">-Password</span></span>
<span data-ttu-id="27af3-125">Hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27af3-125">Password for the user.</span></span>
<span data-ttu-id="27af3-126">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="27af3-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="27af3-127">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="27af3-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="27af3-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="27af3-128">-UserPrincipalName</span></span>
<span data-ttu-id="27af3-129">Główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27af3-129">The user principal name.</span></span>
<span data-ttu-id="27af3-130">Przykład — ' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="27af3-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="27af3-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27af3-131">-Confirm</span></span>
<span data-ttu-id="27af3-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27af3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27af3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27af3-133">-WhatIf</span></span>
<span data-ttu-id="27af3-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27af3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27af3-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27af3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27af3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27af3-136">CommonParameters</span></span>
<span data-ttu-id="27af3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27af3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27af3-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27af3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27af3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27af3-139">INPUTS</span></span>

### <span data-ttu-id="27af3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="27af3-140">System.String</span></span>

### <span data-ttu-id="27af3-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="27af3-141">System.Security.SecureString</span></span>

### <span data-ttu-id="27af3-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="27af3-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="27af3-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27af3-143">OUTPUTS</span></span>

### <span data-ttu-id="27af3-144">Microsoft. Azure. Commands. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="27af3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="27af3-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27af3-145">NOTES</span></span>

## <span data-ttu-id="27af3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27af3-146">RELATED LINKS</span></span>

[<span data-ttu-id="27af3-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27af3-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="27af3-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27af3-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="27af3-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27af3-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
