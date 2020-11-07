---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
ms.openlocfilehash: a557676d35eb167438f29c36a729ee652a45d591
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898438"
---
# <span data-ttu-id="c0f4a-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="c0f4a-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="c0f4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f4a-103">Odkrycie usuniętego magazynu kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0f4a-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0f4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f4a-106">Polecenie cmdlet **Undo-AzureRmKeyVaultRemoval** powoduje odzyskanie uprzednio usuniętego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="c0f4a-107">Odzyskany magazyn będzie aktywny po odzyskaniu</span><span class="sxs-lookup"><span data-stu-id="c0f4a-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="c0f4a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0f4a-108">EXAMPLES</span></span>

### <span data-ttu-id="c0f4a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0f4a-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="c0f4a-110">To polecenie odzyska Magazyn kluczy "MyKeyVault", który został wcześniej usunięty z obszaru eastus2 i grupy zasobów "moja grupa zasobów", w stan aktywny i dostępny.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="c0f4a-111">Znaczniki są również zastępowane nowym znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="c0f4a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0f4a-112">PARAMETERS</span></span>

### <span data-ttu-id="c0f4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f4a-113">-DefaultProfile</span></span>
<span data-ttu-id="c0f4a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0f4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0f4a-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c0f4a-115">-Location</span></span>
<span data-ttu-id="c0f4a-116">Określa oryginalny region usługi Azure w magazynie usunięty.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0f4a-118">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f4a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0f4a-119">-Tag</span></span>
<span data-ttu-id="c0f4a-120">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c0f4a-121">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c0f4a-121">For example:</span></span>

<span data-ttu-id="c0f4a-122">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="c0f4a-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f4a-123">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="c0f4a-123">-VaultName</span></span>
<span data-ttu-id="c0f4a-124">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-124">Vault name.</span></span>
<span data-ttu-id="c0f4a-125">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c0f4a-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0f4a-126">-Confirm</span></span>
<span data-ttu-id="c0f4a-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0f4a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0f4a-128">-WhatIf</span></span>
<span data-ttu-id="c0f4a-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0f4a-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0f4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f4a-131">CommonParameters</span></span>
<span data-ttu-id="c0f4a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f4a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f4a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0f4a-134">INPUTS</span></span>

### <span data-ttu-id="c0f4a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c0f4a-135">System.String</span></span>
<span data-ttu-id="c0f4a-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0f4a-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0f4a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0f4a-137">OUTPUTS</span></span>

### <span data-ttu-id="c0f4a-138">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="c0f4a-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="c0f4a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0f4a-139">NOTES</span></span>

## <span data-ttu-id="c0f4a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0f4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0f4a-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c0f4a-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="c0f4a-142">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c0f4a-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="c0f4a-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c0f4a-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
