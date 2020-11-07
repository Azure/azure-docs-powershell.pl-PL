---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 5a1f0b5bac62c4b10912fbbffc07cda7c1f2fb7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898863"
---
# <span data-ttu-id="a2000-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a2000-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="a2000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2000-102">SYNOPSIS</span></span>
<span data-ttu-id="a2000-103">Tworzy nowego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2000-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2000-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2000-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2000-105">DESCRIPTION</span></span>
<span data-ttu-id="a2000-106">Tworzy nowego użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="a2000-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="a2000-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="a2000-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="a2000-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2000-108">EXAMPLES</span></span>

### <span data-ttu-id="a2000-109">Przykład 1 — Tworzenie nowego użytkownika usługi AD</span><span class="sxs-lookup"><span data-stu-id="a2000-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="a2000-110">Tworzy nowego użytkownika usługi AD o nazwie "WebDisplayName" i głównej nazwie użytkownika " myemail@domain.com " w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="a2000-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="a2000-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2000-111">PARAMETERS</span></span>

### <span data-ttu-id="a2000-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2000-112">-DefaultProfile</span></span>
<span data-ttu-id="a2000-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a2000-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2000-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2000-114">-DisplayName</span></span>
<span data-ttu-id="a2000-115">Nazwa wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2000-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="a2000-116">przykład "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="a2000-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="a2000-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="a2000-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="a2000-118">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="a2000-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="a2000-119">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="a2000-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="a2000-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="a2000-120">-ImmutableId</span></span>
<span data-ttu-id="a2000-121">Należy ją określić tylko wtedy, gdy używana jest domena federacyjna dla właściwości głównej nazwy użytkownika (UPN) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2000-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="a2000-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="a2000-122">-MailNickname</span></span>
<span data-ttu-id="a2000-123">Alias e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2000-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="a2000-124">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="a2000-124">-Password</span></span>
<span data-ttu-id="a2000-125">Hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2000-125">Password for the user.</span></span>
<span data-ttu-id="a2000-126">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a2000-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="a2000-127">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="a2000-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="a2000-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a2000-128">-UserPrincipalName</span></span>
<span data-ttu-id="a2000-129">Główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2000-129">The user principal name.</span></span>
<span data-ttu-id="a2000-130">Przykład — ' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="a2000-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="a2000-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2000-131">-Confirm</span></span>
<span data-ttu-id="a2000-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2000-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2000-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2000-133">-WhatIf</span></span>
<span data-ttu-id="a2000-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2000-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2000-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2000-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2000-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2000-136">CommonParameters</span></span>
<span data-ttu-id="a2000-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2000-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2000-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2000-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2000-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2000-139">INPUTS</span></span>

### <span data-ttu-id="a2000-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a2000-140">System.String</span></span>

### <span data-ttu-id="a2000-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a2000-141">System.Security.SecureString</span></span>

### <span data-ttu-id="a2000-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2000-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2000-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2000-143">OUTPUTS</span></span>

### <span data-ttu-id="a2000-144">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a2000-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a2000-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2000-145">NOTES</span></span>

## <span data-ttu-id="a2000-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2000-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2000-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a2000-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



[<span data-ttu-id="a2000-148">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a2000-148">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
