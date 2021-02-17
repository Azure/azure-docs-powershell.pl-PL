---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 92c5166794808d08a925c458afc14fe4b6dca834
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408733"
---
# <span data-ttu-id="1679d-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="1679d-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="1679d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1679d-102">SYNOPSIS</span></span>
<span data-ttu-id="1679d-103">Przywraca usunięty klucz tajny w magazynie kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="1679d-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="1679d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1679d-104">SYNTAX</span></span>

### <span data-ttu-id="1679d-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1679d-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1679d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1679d-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1679d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1679d-107">DESCRIPTION</span></span>
<span data-ttu-id="1679d-108">Polecenie **cmdlet Undo-AzKeyVaultSecretRemoval** odzyska usunięty wcześniej klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="1679d-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="1679d-109">Odzyskany klucz tajny będzie aktywny i będzie można go używać we wszystkich normalnych operacjach tajnych.</span><span class="sxs-lookup"><span data-stu-id="1679d-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="1679d-110">Aby wykonać tę operację, dzwoniący musi mieć uprawnienie do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1679d-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1679d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1679d-111">EXAMPLES</span></span>

### <span data-ttu-id="1679d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1679d-112">Example 1</span></span>
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

<span data-ttu-id="1679d-113">To polecenie spowoduje odzyskanie poprzednio usuniętego stanu "MySecret", który był aktywny i użyteczny.</span><span class="sxs-lookup"><span data-stu-id="1679d-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1679d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1679d-114">PARAMETERS</span></span>

### <span data-ttu-id="1679d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1679d-115">-DefaultProfile</span></span>
<span data-ttu-id="1679d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1679d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1679d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1679d-117">-InputObject</span></span>
<span data-ttu-id="1679d-118">Usunięto tajny obiekt</span><span class="sxs-lookup"><span data-stu-id="1679d-118">Deleted secret object</span></span>

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

### <span data-ttu-id="1679d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1679d-119">-Name</span></span>
<span data-ttu-id="1679d-120">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="1679d-120">Secret name.</span></span>
<span data-ttu-id="1679d-121">Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybranego środowiska i nazwy tajnej.</span><span class="sxs-lookup"><span data-stu-id="1679d-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="1679d-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1679d-122">-VaultName</span></span>
<span data-ttu-id="1679d-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="1679d-123">Vault name.</span></span>
<span data-ttu-id="1679d-124">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="1679d-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1679d-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1679d-125">-Confirm</span></span>
<span data-ttu-id="1679d-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1679d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1679d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1679d-127">-WhatIf</span></span>
<span data-ttu-id="1679d-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1679d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1679d-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1679d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1679d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1679d-130">CommonParameters</span></span>
<span data-ttu-id="1679d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1679d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1679d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1679d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1679d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1679d-133">INPUTS</span></span>

### <span data-ttu-id="1679d-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1679d-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="1679d-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1679d-135">OUTPUTS</span></span>

### <span data-ttu-id="1679d-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1679d-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="1679d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1679d-137">NOTES</span></span>

## <span data-ttu-id="1679d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1679d-138">RELATED LINKS</span></span>

[<span data-ttu-id="1679d-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1679d-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="1679d-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1679d-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
