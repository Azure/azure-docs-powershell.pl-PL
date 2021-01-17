---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491282"
---
# <span data-ttu-id="83591-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="83591-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="83591-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83591-102">SYNOPSIS</span></span>
<span data-ttu-id="83591-103">Odwołaj wszystkie klucze delegowania użytkowników konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="83591-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="83591-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83591-104">SYNTAX</span></span>

### <span data-ttu-id="83591-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="83591-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83591-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="83591-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83591-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="83591-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83591-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83591-108">DESCRIPTION</span></span>
<span data-ttu-id="83591-109">Polecenie cmdlet **REVOKE-AzStorageAccountUserDelegationKeys** powoduje odebranie wszystkich kluczy delegowania użytkowników konta magazynu, więc wszystkie tokeny SAS tożsamości konta magazynu również zostaną odwołane.</span><span class="sxs-lookup"><span data-stu-id="83591-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="83591-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83591-110">EXAMPLES</span></span>

### <span data-ttu-id="83591-111">Przykład 1: odwoływanie wszystkich kluczy delegowania użytkowników konta magazynu</span><span class="sxs-lookup"><span data-stu-id="83591-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="83591-112">W tym przykładzie odebrano wszystkie klucze delegowania użytkowników konta magazynu, więc wszystkie tokeny SAS tożsamości wygenerowane za pomocą kluczy delegowania użytkownika również zostaną odwołane.</span><span class="sxs-lookup"><span data-stu-id="83591-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="83591-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83591-113">PARAMETERS</span></span>

### <span data-ttu-id="83591-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83591-114">-DefaultProfile</span></span>
<span data-ttu-id="83591-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83591-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83591-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83591-116">-InputObject</span></span>
<span data-ttu-id="83591-117">Obiekt konta magazynu zwrócony przez Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="83591-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83591-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83591-118">-PassThru</span></span>
<span data-ttu-id="83591-119">Zazwyczaj to polecenie cmdlet nie zwraca żadnych danych wyjściowych w przypadku poprawnego wykonania, ten parametr wymusza, aby polecenie cmdlet zwracało wartość ($true) po poprawnym zakończeniu.</span><span class="sxs-lookup"><span data-stu-id="83591-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83591-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83591-120">-ResourceGroupName</span></span>
<span data-ttu-id="83591-121">Nazwa grupy zasobów zawierająca zasób konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="83591-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83591-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83591-122">-ResourceId</span></span>
<span data-ttu-id="83591-123">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="83591-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83591-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83591-124">-StorageAccountName</span></span>
<span data-ttu-id="83591-125">Nazwa zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="83591-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83591-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83591-126">-Confirm</span></span>
<span data-ttu-id="83591-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83591-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83591-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83591-128">-WhatIf</span></span>
<span data-ttu-id="83591-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83591-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83591-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83591-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83591-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83591-131">CommonParameters</span></span>
<span data-ttu-id="83591-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83591-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83591-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83591-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83591-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83591-134">INPUTS</span></span>

### <span data-ttu-id="83591-135">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83591-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="83591-136">System. String</span><span class="sxs-lookup"><span data-stu-id="83591-136">System.String</span></span>

## <span data-ttu-id="83591-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83591-137">OUTPUTS</span></span>

### <span data-ttu-id="83591-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83591-138">System.Boolean</span></span>

## <span data-ttu-id="83591-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83591-139">NOTES</span></span>

## <span data-ttu-id="83591-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83591-140">RELATED LINKS</span></span>
