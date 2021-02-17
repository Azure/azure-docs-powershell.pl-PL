---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9513cba1532ec70acb77cdf97d19de25db36434f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415584"
---
# <span data-ttu-id="96b36-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="96b36-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="96b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b36-102">SYNOPSIS</span></span>
<span data-ttu-id="96b36-103">Przywraca usunięty klucz tajny w magazynie kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="96b36-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="96b36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96b36-104">SYNTAX</span></span>

### <span data-ttu-id="96b36-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="96b36-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b36-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="96b36-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b36-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="96b36-107">DESCRIPTION</span></span>
<span data-ttu-id="96b36-108">Polecenie **cmdlet Undo-AzKeyVaultSecretRemoval** spowoduje odzyskanie poprzednio usuniętego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="96b36-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="96b36-109">Odzyskany klucz tajny będzie aktywny i będzie można go używać we wszystkich normalnych operacjach tajnych.</span><span class="sxs-lookup"><span data-stu-id="96b36-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="96b36-110">Aby wykonać tę operację, dzwoniący musi mieć uprawnienie do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="96b36-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="96b36-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96b36-111">EXAMPLES</span></span>

### <span data-ttu-id="96b36-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96b36-112">Example 1</span></span>
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

<span data-ttu-id="96b36-113">To polecenie spowoduje odzyskanie poprzednio usuniętego stanu "MySecret", który był aktywny i użyteczny.</span><span class="sxs-lookup"><span data-stu-id="96b36-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="96b36-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96b36-114">PARAMETERS</span></span>

### <span data-ttu-id="96b36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b36-115">-DefaultProfile</span></span>
<span data-ttu-id="96b36-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="96b36-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96b36-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96b36-117">-InputObject</span></span>
<span data-ttu-id="96b36-118">Usunięto tajny obiekt</span><span class="sxs-lookup"><span data-stu-id="96b36-118">Deleted secret object</span></span>

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

### <span data-ttu-id="96b36-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="96b36-119">-Name</span></span>
<span data-ttu-id="96b36-120">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="96b36-120">Secret name.</span></span>
<span data-ttu-id="96b36-121">Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybranego środowiska i nazwy tajnej.</span><span class="sxs-lookup"><span data-stu-id="96b36-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="96b36-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="96b36-122">-VaultName</span></span>
<span data-ttu-id="96b36-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="96b36-123">Vault name.</span></span>
<span data-ttu-id="96b36-124">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="96b36-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="96b36-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96b36-125">-Confirm</span></span>
<span data-ttu-id="96b36-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96b36-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b36-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b36-127">-WhatIf</span></span>
<span data-ttu-id="96b36-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96b36-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b36-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="96b36-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b36-130">CommonParameters</span></span>
<span data-ttu-id="96b36-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b36-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96b36-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b36-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96b36-133">INPUTS</span></span>

### <span data-ttu-id="96b36-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="96b36-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="96b36-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96b36-135">OUTPUTS</span></span>

### <span data-ttu-id="96b36-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96b36-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="96b36-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96b36-137">NOTES</span></span>

## <span data-ttu-id="96b36-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96b36-138">RELATED LINKS</span></span>

[<span data-ttu-id="96b36-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96b36-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="96b36-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="96b36-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
