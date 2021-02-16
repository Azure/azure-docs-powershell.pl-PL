---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399094"
---
# <span data-ttu-id="01b57-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="01b57-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="01b57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b57-102">SYNOPSIS</span></span>
<span data-ttu-id="01b57-103">Przywraca usunięty klucz tajny w magazynie kluczy do stanu aktywnego.</span><span class="sxs-lookup"><span data-stu-id="01b57-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="01b57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01b57-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01b57-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="01b57-105">DESCRIPTION</span></span>
<span data-ttu-id="01b57-106">Polecenie **cmdlet Undo-AzKeyVaultSecretRemoval** odzyska usunięty wcześniej klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="01b57-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="01b57-107">Odzyskany klucz tajny będzie aktywny i będzie można go używać we wszystkich normalnych operacjach tajnych.</span><span class="sxs-lookup"><span data-stu-id="01b57-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="01b57-108">Aby wykonać tę operację, dzwoniący musi mieć uprawnienie do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="01b57-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="01b57-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01b57-109">EXAMPLES</span></span>

### <span data-ttu-id="01b57-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01b57-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="01b57-111">To polecenie spowoduje odzyskanie poprzednio usuniętego stanu "MySecret", który był aktywny i użyteczny.</span><span class="sxs-lookup"><span data-stu-id="01b57-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="01b57-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b57-112">PARAMETERS</span></span>

### <span data-ttu-id="01b57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b57-113">-DefaultProfile</span></span>
<span data-ttu-id="01b57-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="01b57-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b57-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="01b57-115">-Name</span></span>
<span data-ttu-id="01b57-116">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="01b57-116">Secret name.</span></span>
<span data-ttu-id="01b57-117">Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybranego środowiska i nazwy tajnej.</span><span class="sxs-lookup"><span data-stu-id="01b57-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b57-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="01b57-118">-VaultName</span></span>
<span data-ttu-id="01b57-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="01b57-119">Vault name.</span></span>
<span data-ttu-id="01b57-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="01b57-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b57-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01b57-121">-Confirm</span></span>
<span data-ttu-id="01b57-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01b57-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b57-123">-WhatIf</span></span>
<span data-ttu-id="01b57-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b57-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b57-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01b57-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b57-126">CommonParameters</span></span>
<span data-ttu-id="01b57-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b57-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01b57-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b57-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01b57-129">INPUTS</span></span>

### <span data-ttu-id="01b57-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01b57-130">System.String</span></span>

## <span data-ttu-id="01b57-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01b57-131">OUTPUTS</span></span>

### <span data-ttu-id="01b57-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="01b57-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="01b57-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01b57-133">NOTES</span></span>

## <span data-ttu-id="01b57-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01b57-134">RELATED LINKS</span></span>

[<span data-ttu-id="01b57-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="01b57-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="01b57-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="01b57-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
