---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553771"
---
# <span data-ttu-id="a42f1-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="a42f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a42f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a42f1-103">Tworzy nowego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a42f1-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a42f1-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a42f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a42f1-105">DESCRIPTION</span></span>
<span data-ttu-id="a42f1-106">Tworzy nowego użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="a42f1-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="a42f1-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="a42f1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a42f1-108">EXAMPLES</span></span>

### <span data-ttu-id="a42f1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a42f1-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a42f1-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="a42f1-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="a42f1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a42f1-111">PARAMETERS</span></span>

### <span data-ttu-id="a42f1-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a42f1-112">-DisplayName</span></span>
<span data-ttu-id="a42f1-113">Nazwa wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a42f1-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="a42f1-114">przykład "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="a42f1-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="a42f1-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="a42f1-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="a42f1-116">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="a42f1-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="a42f1-117">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="a42f1-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="a42f1-118">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="a42f1-118">-ImmutableId</span></span>
<span data-ttu-id="a42f1-119">Należy ją określić tylko wtedy, gdy używana jest domena federacyjna dla właściwości głównej nazwy użytkownika (UPN) użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a42f1-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="a42f1-120">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="a42f1-120">-Password</span></span>
<span data-ttu-id="a42f1-121">Hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a42f1-121">Password for the user.</span></span>
<span data-ttu-id="a42f1-122">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a42f1-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="a42f1-123">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="a42f1-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="a42f1-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a42f1-124">-UserPrincipalName</span></span>
<span data-ttu-id="a42f1-125">Główna nazwa użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a42f1-125">The user principal name.</span></span>
<span data-ttu-id="a42f1-126">Przykład — ' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="a42f1-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="a42f1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a42f1-127">-Confirm</span></span>
<span data-ttu-id="a42f1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42f1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a42f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a42f1-129">-WhatIf</span></span>
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

### <span data-ttu-id="a42f1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42f1-130">-DefaultProfile</span></span>
<span data-ttu-id="a42f1-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a42f1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a42f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42f1-132">CommonParameters</span></span>
<span data-ttu-id="a42f1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42f1-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42f1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42f1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a42f1-135">INPUTS</span></span>

## <span data-ttu-id="a42f1-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a42f1-136">OUTPUTS</span></span>

### <span data-ttu-id="a42f1-137">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a42f1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a42f1-138">NOTES</span></span>

## <span data-ttu-id="a42f1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a42f1-139">RELATED LINKS</span></span>

[<span data-ttu-id="a42f1-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="a42f1-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="a42f1-142">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a42f1-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
