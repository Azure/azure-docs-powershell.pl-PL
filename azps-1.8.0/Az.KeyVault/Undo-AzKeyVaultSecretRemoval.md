---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 26bf7b91b330032e05f96f425cb21908fc3df55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867851"
---
# <span data-ttu-id="a5ffe-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a5ffe-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="a5ffe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ffe-103">Odkrycie usuniętego klucza tajnego w magazynie kluczy w stan aktywny.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="a5ffe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5ffe-104">SYNTAX</span></span>

### <span data-ttu-id="a5ffe-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a5ffe-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ffe-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5ffe-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ffe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a5ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ffe-108">Polecenie cmdlet **Undo-AzKeyVaultSecretRemoval** powoduje odzyskanie usuniętego wcześniej klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="a5ffe-109">Odzyskany klucz tajny będzie aktywny i może być stosowany do wszystkich zwykłych działań tajnych.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="a5ffe-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="a5ffe-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a5ffe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5ffe-111">EXAMPLES</span></span>

### <span data-ttu-id="a5ffe-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5ffe-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="a5ffe-113">To polecenie odzyska tajne hasło, które zostało wcześniej usunięte, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a5ffe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5ffe-114">PARAMETERS</span></span>

### <span data-ttu-id="a5ffe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ffe-115">-DefaultProfile</span></span>
<span data-ttu-id="a5ffe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a5ffe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5ffe-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5ffe-117">-InputObject</span></span>
<span data-ttu-id="a5ffe-118">Usunięto obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="a5ffe-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ffe-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5ffe-119">-Name</span></span>
<span data-ttu-id="a5ffe-120">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-120">Secret name.</span></span>
<span data-ttu-id="a5ffe-121">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ffe-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a5ffe-122">-VaultName</span></span>
<span data-ttu-id="a5ffe-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-123">Vault name.</span></span>
<span data-ttu-id="a5ffe-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ffe-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5ffe-125">-Confirm</span></span>
<span data-ttu-id="a5ffe-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ffe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ffe-127">-WhatIf</span></span>
<span data-ttu-id="a5ffe-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ffe-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ffe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ffe-130">CommonParameters</span></span>
<span data-ttu-id="a5ffe-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ffe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ffe-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ffe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ffe-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5ffe-133">INPUTS</span></span>

### <span data-ttu-id="a5ffe-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a5ffe-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="a5ffe-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5ffe-135">OUTPUTS</span></span>

### <span data-ttu-id="a5ffe-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a5ffe-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="a5ffe-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5ffe-137">NOTES</span></span>

## <span data-ttu-id="a5ffe-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5ffe-138">RELATED LINKS</span></span>

[<span data-ttu-id="a5ffe-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a5ffe-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a5ffe-140">Dodaj-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a5ffe-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="a5ffe-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a5ffe-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
