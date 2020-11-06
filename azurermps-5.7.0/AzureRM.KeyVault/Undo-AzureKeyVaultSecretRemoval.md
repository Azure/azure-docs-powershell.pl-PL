---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548088"
---
# <span data-ttu-id="caa13-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="caa13-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="caa13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="caa13-102">SYNOPSIS</span></span>
<span data-ttu-id="caa13-103">Odkrycie usuniętego klucza tajnego w magazynie kluczy w stan aktywny.</span><span class="sxs-lookup"><span data-stu-id="caa13-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="caa13-104">SYNTAX</span></span>

### <span data-ttu-id="caa13-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="caa13-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caa13-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="caa13-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caa13-107">Opis</span><span class="sxs-lookup"><span data-stu-id="caa13-107">DESCRIPTION</span></span>
<span data-ttu-id="caa13-108">Polecenie cmdlet **Undo-AzureKeyVaultSecretRemoval** powoduje odzyskanie usuniętego wcześniej klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="caa13-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="caa13-109">Odzyskany klucz tajny będzie aktywny i może być stosowany do wszystkich zwykłych działań tajnych.</span><span class="sxs-lookup"><span data-stu-id="caa13-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="caa13-110">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="caa13-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="caa13-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="caa13-111">EXAMPLES</span></span>

### <span data-ttu-id="caa13-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="caa13-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="caa13-113">To polecenie odzyska tajne hasło, które zostało wcześniej usunięte, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="caa13-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="caa13-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="caa13-114">PARAMETERS</span></span>

### <span data-ttu-id="caa13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa13-115">-DefaultProfile</span></span>
<span data-ttu-id="caa13-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="caa13-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caa13-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="caa13-117">-InputObject</span></span>
<span data-ttu-id="caa13-118">Usunięto obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="caa13-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caa13-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="caa13-119">-Name</span></span>
<span data-ttu-id="caa13-120">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="caa13-120">Secret name.</span></span>
<span data-ttu-id="caa13-121">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="caa13-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caa13-122">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="caa13-122">-VaultName</span></span>
<span data-ttu-id="caa13-123">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="caa13-123">Vault name.</span></span>
<span data-ttu-id="caa13-124">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="caa13-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caa13-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="caa13-125">-Confirm</span></span>
<span data-ttu-id="caa13-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caa13-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa13-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa13-127">-WhatIf</span></span>
<span data-ttu-id="caa13-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caa13-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa13-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="caa13-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa13-130">CommonParameters</span></span>
<span data-ttu-id="caa13-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa13-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa13-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa13-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="caa13-133">INPUTS</span></span>

### <span data-ttu-id="caa13-134">System. String</span><span class="sxs-lookup"><span data-stu-id="caa13-134">System.String</span></span>

## <span data-ttu-id="caa13-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="caa13-135">OUTPUTS</span></span>

### <span data-ttu-id="caa13-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="caa13-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="caa13-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="caa13-137">NOTES</span></span>

## <span data-ttu-id="caa13-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="caa13-138">RELATED LINKS</span></span>

[<span data-ttu-id="caa13-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="caa13-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="caa13-140">Dodaj-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="caa13-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="caa13-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="caa13-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
