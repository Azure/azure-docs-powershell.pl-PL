---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892989"
---
# <span data-ttu-id="a4d4e-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a4d4e-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="a4d4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d4e-103">Odkrycie usuniętego klucza tajnego w magazynie kluczy w stan aktywny.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="a4d4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4d4e-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d4e-106">Polecenie cmdlet **Undo-AzKeyVaultSecretRemoval** powoduje odzyskanie usuniętego wcześniej klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="a4d4e-107">Odzyskany klucz tajny będzie aktywny i może być stosowany do wszystkich zwykłych działań tajnych.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="a4d4e-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="a4d4e-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a4d4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="a4d4e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4d4e-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="a4d4e-111">To polecenie odzyska tajne hasło, które zostało wcześniej usunięte, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a4d4e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4d4e-112">PARAMETERS</span></span>

### <span data-ttu-id="a4d4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d4e-113">-DefaultProfile</span></span>
<span data-ttu-id="a4d4e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4d4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4d4e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4d4e-115">-Name</span></span>
<span data-ttu-id="a4d4e-116">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-116">Secret name.</span></span>
<span data-ttu-id="a4d4e-117">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="a4d4e-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a4d4e-118">-VaultName</span></span>
<span data-ttu-id="a4d4e-119">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-119">Vault name.</span></span>
<span data-ttu-id="a4d4e-120">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a4d4e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4d4e-121">-Confirm</span></span>
<span data-ttu-id="a4d4e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d4e-123">-WhatIf</span></span>
<span data-ttu-id="a4d4e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d4e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d4e-126">CommonParameters</span></span>
<span data-ttu-id="a4d4e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d4e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d4e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d4e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4d4e-129">INPUTS</span></span>

### <span data-ttu-id="a4d4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d4e-130">System.String</span></span>

## <span data-ttu-id="a4d4e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4d4e-131">OUTPUTS</span></span>

### <span data-ttu-id="a4d4e-132">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="a4d4e-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="a4d4e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4d4e-133">NOTES</span></span>

## <span data-ttu-id="a4d4e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4d4e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a4d4e-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a4d4e-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a4d4e-136">Dodaj-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a4d4e-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="a4d4e-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a4d4e-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
