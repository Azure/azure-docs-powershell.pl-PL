---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716665"
---
# <span data-ttu-id="b589a-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b589a-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="b589a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b589a-102">SYNOPSIS</span></span>
<span data-ttu-id="b589a-103">Aktualizuje istniejącego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b589a-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b589a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b589a-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b589a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b589a-105">DESCRIPTION</span></span>
<span data-ttu-id="b589a-106">Aktualizuje istniejącego użytkownika usługi Active Directory (konto służbowe jest znane również pod nazwą org-ID).</span><span class="sxs-lookup"><span data-stu-id="b589a-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="b589a-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="b589a-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="b589a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b589a-108">EXAMPLES</span></span>

### <span data-ttu-id="b589a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b589a-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b589a-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="b589a-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="b589a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b589a-111">PARAMETERS</span></span>

### <span data-ttu-id="b589a-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b589a-112">-DisplayName</span></span>
<span data-ttu-id="b589a-113">Nowa nazwa, która ma być wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b589a-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="b589a-114">Przykład — 'Alex Wu ".</span><span class="sxs-lookup"><span data-stu-id="b589a-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="b589a-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="b589a-115">-EnableAccount</span></span>
<span data-ttu-id="b589a-116">Prawda, aby włączyć konto; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="b589a-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b589a-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="b589a-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="b589a-118">Należy go określić tylko w przypadku aktualizowania hasła.</span><span class="sxs-lookup"><span data-stu-id="b589a-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="b589a-119">W przeciwnym razie zostanie zignorowana.</span><span class="sxs-lookup"><span data-stu-id="b589a-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="b589a-120">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="b589a-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="b589a-121">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="b589a-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="b589a-122">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="b589a-122">-Password</span></span>
<span data-ttu-id="b589a-123">Nowe hasło dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b589a-123">New password for the user.</span></span>
<span data-ttu-id="b589a-124">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b589a-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="b589a-125">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="b589a-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="b589a-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="b589a-126">-UPNOrObjectId</span></span>
<span data-ttu-id="b589a-127">Główna nazwa użytkownika (na przykład ' someuser@contoso.com ') lub identyfikator objectid użytkownika, dla którego właściwości muszą być zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="b589a-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="b589a-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b589a-128">-Confirm</span></span>
<span data-ttu-id="b589a-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b589a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b589a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b589a-130">-WhatIf</span></span>
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

### <span data-ttu-id="b589a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b589a-131">-DefaultProfile</span></span>
<span data-ttu-id="b589a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b589a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b589a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b589a-133">CommonParameters</span></span>
<span data-ttu-id="b589a-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b589a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b589a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b589a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b589a-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b589a-136">INPUTS</span></span>

## <span data-ttu-id="b589a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b589a-137">OUTPUTS</span></span>

### <span data-ttu-id="b589a-138">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="b589a-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b589a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b589a-139">NOTES</span></span>

## <span data-ttu-id="b589a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b589a-140">RELATED LINKS</span></span>

[<span data-ttu-id="b589a-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b589a-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="b589a-142">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b589a-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="b589a-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b589a-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

