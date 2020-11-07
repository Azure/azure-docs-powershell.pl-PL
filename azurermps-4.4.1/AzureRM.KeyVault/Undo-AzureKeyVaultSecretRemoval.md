---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718192"
---
# <span data-ttu-id="1ea0d-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="1ea0d-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="1ea0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ea0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea0d-103">Odkrycie usuniętego klucza tajnego w magazynie kluczy w stan aktywny.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ea0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ea0d-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ea0d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea0d-106">Polecenie cmdlet **Undo-AzureKeyVaultSecretRemoval** powoduje odzyskanie usuniętego wcześniej klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="1ea0d-107">Odzyskany klucz tajny będzie aktywny i może być stosowany do wszystkich zwykłych działań tajnych.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="1ea0d-108">Aby można było wykonać tę operację, osoba dzwoniąca musi mieć uprawnienie "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="1ea0d-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1ea0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ea0d-109">EXAMPLES</span></span>

### <span data-ttu-id="1ea0d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ea0d-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="1ea0d-111">To polecenie odzyska tajne hasło, które zostało wcześniej usunięte, w stanie aktywnym i zdatnym do użycia.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1ea0d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ea0d-112">PARAMETERS</span></span>

### <span data-ttu-id="1ea0d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ea0d-113">-Name</span></span>
<span data-ttu-id="1ea0d-114">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-114">Secret name.</span></span>
<span data-ttu-id="1ea0d-115">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea0d-116">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1ea0d-116">-VaultName</span></span>
<span data-ttu-id="1ea0d-117">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-117">Vault name.</span></span>
<span data-ttu-id="1ea0d-118">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea0d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ea0d-119">-Confirm</span></span>
<span data-ttu-id="1ea0d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea0d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea0d-121">-WhatIf</span></span>
<span data-ttu-id="1ea0d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea0d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea0d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea0d-124">-DefaultProfile</span></span>
<span data-ttu-id="1ea0d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ea0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea0d-126">CommonParameters</span></span>
<span data-ttu-id="1ea0d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea0d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea0d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea0d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ea0d-129">INPUTS</span></span>

### <span data-ttu-id="1ea0d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea0d-130">System.String</span></span>

## <span data-ttu-id="1ea0d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ea0d-131">OUTPUTS</span></span>

### <span data-ttu-id="1ea0d-132">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="1ea0d-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="1ea0d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ea0d-133">NOTES</span></span>

## <span data-ttu-id="1ea0d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ea0d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ea0d-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea0d-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="1ea0d-136">Dodaj-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea0d-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="1ea0d-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ea0d-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
