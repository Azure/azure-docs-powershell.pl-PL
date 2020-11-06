---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544127"
---
# <span data-ttu-id="25e96-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="25e96-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="25e96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25e96-102">SYNOPSIS</span></span>
<span data-ttu-id="25e96-103">Tworzy nowego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25e96-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25e96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25e96-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25e96-105">DESCRIPTION</span></span>
<span data-ttu-id="25e96-106">Tworzy nowego użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="25e96-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="25e96-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="25e96-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="25e96-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25e96-108">EXAMPLES</span></span>

### <span data-ttu-id="25e96-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25e96-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="25e96-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="25e96-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="25e96-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25e96-111">PARAMETERS</span></span>

### <span data-ttu-id="25e96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e96-112">-DefaultProfile</span></span>
<span data-ttu-id="25e96-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25e96-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="25e96-114">-DisplayName</span></span>
<span data-ttu-id="25e96-115">Nazwa wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25e96-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="25e96-116">przykład "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="25e96-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="25e96-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="25e96-118">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="25e96-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="25e96-119">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="25e96-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="25e96-120">-ImmutableId</span></span>
<span data-ttu-id="25e96-121">Należy ją określić tylko wtedy, gdy używana jest domena federacyjna dla właściwości głównej nazwy użytkownika (UPN) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25e96-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-122">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="25e96-122">-Password</span></span>
<span data-ttu-id="25e96-123">Hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25e96-123">Password for the user.</span></span>
<span data-ttu-id="25e96-124">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="25e96-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="25e96-125">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="25e96-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="25e96-126">-UserPrincipalName</span></span>
<span data-ttu-id="25e96-127">Główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25e96-127">The user principal name.</span></span>
<span data-ttu-id="25e96-128">Przykład — ' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="25e96-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25e96-129">-Confirm</span></span>
<span data-ttu-id="25e96-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e96-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e96-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e96-132">CommonParameters</span></span>
<span data-ttu-id="25e96-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e96-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e96-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e96-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25e96-135">INPUTS</span></span>

### <span data-ttu-id="25e96-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="25e96-136">None</span></span>
<span data-ttu-id="25e96-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="25e96-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25e96-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25e96-138">OUTPUTS</span></span>

### <span data-ttu-id="25e96-139">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="25e96-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="25e96-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25e96-140">NOTES</span></span>

## <span data-ttu-id="25e96-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25e96-141">RELATED LINKS</span></span>

[<span data-ttu-id="25e96-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="25e96-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="25e96-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="25e96-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="25e96-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="25e96-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
