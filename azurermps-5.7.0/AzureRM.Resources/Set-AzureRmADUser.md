---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524954"
---
# <span data-ttu-id="f903c-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f903c-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="f903c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f903c-102">SYNOPSIS</span></span>
<span data-ttu-id="f903c-103">Aktualizuje istniejącego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f903c-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f903c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f903c-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f903c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f903c-105">DESCRIPTION</span></span>
<span data-ttu-id="f903c-106">Aktualizuje istniejącego użytkownika usługi Active Directory (konto służbowe jest znane również pod nazwą org-ID).</span><span class="sxs-lookup"><span data-stu-id="f903c-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="f903c-107">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="f903c-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="f903c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f903c-108">EXAMPLES</span></span>

### <span data-ttu-id="f903c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f903c-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f903c-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="f903c-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="f903c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f903c-111">PARAMETERS</span></span>

### <span data-ttu-id="f903c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f903c-112">-DefaultProfile</span></span>
<span data-ttu-id="f903c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f903c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f903c-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f903c-114">-DisplayName</span></span>
<span data-ttu-id="f903c-115">Nowa nazwa, która ma być wyświetlana w książce adresowej użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f903c-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="f903c-116">Przykład — 'Alex Wu ".</span><span class="sxs-lookup"><span data-stu-id="f903c-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="f903c-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="f903c-117">-EnableAccount</span></span>
<span data-ttu-id="f903c-118">Prawda, aby włączyć konto; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="f903c-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f903c-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="f903c-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="f903c-120">Należy go określić tylko w przypadku aktualizowania hasła.</span><span class="sxs-lookup"><span data-stu-id="f903c-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="f903c-121">W przeciwnym razie zostanie zignorowana.</span><span class="sxs-lookup"><span data-stu-id="f903c-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="f903c-122">Należy określić, czy użytkownik musi zmienić hasło w następnym poprawnym logowaniu (true).</span><span class="sxs-lookup"><span data-stu-id="f903c-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="f903c-123">Zachowanie domyślne to (FAŁSZ), aby nie zmieniać hasła przy następnym pomyślnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="f903c-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="f903c-124">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f903c-124">-Password</span></span>
<span data-ttu-id="f903c-125">Nowe hasło dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f903c-125">New password for the user.</span></span>
<span data-ttu-id="f903c-126">Musi ono odpowiadać wymaganiom złożoności hasła dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f903c-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="f903c-127">Zaleca się ustawienie silnego hasła.</span><span class="sxs-lookup"><span data-stu-id="f903c-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f903c-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="f903c-128">-UPNOrObjectId</span></span>
<span data-ttu-id="f903c-129">Główna nazwa użytkownika (na przykład ' someuser@contoso.com ') lub identyfikator objectid użytkownika, dla którego właściwości muszą być zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="f903c-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="f903c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f903c-130">-Confirm</span></span>
<span data-ttu-id="f903c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f903c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f903c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f903c-132">-WhatIf</span></span>
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

### <span data-ttu-id="f903c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f903c-133">CommonParameters</span></span>
<span data-ttu-id="f903c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f903c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f903c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f903c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f903c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f903c-136">INPUTS</span></span>

### <span data-ttu-id="f903c-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f903c-137">None</span></span>
<span data-ttu-id="f903c-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f903c-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f903c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f903c-139">OUTPUTS</span></span>

### <span data-ttu-id="f903c-140">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="f903c-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="f903c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f903c-141">NOTES</span></span>

## <span data-ttu-id="f903c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f903c-142">RELATED LINKS</span></span>

[<span data-ttu-id="f903c-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f903c-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="f903c-144">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f903c-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="f903c-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f903c-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

