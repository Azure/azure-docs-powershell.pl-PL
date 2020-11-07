---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716840"
---
# <span data-ttu-id="a125e-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a125e-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a125e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a125e-102">SYNOPSIS</span></span>
<span data-ttu-id="a125e-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a125e-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a125e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a125e-104">SYNTAX</span></span>

### <span data-ttu-id="a125e-105">Magazynname (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a125e-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a125e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a125e-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a125e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a125e-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a125e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a125e-108">DESCRIPTION</span></span>
<span data-ttu-id="a125e-109">Polecenie cmdlet **Get-AzureKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="a125e-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a125e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a125e-110">EXAMPLES</span></span>

### <span data-ttu-id="a125e-111">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="a125e-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="a125e-112">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="a125e-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="a125e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a125e-113">PARAMETERS</span></span>

### <span data-ttu-id="a125e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a125e-114">-DefaultProfile</span></span>
<span data-ttu-id="a125e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a125e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a125e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a125e-116">-InputObject</span></span>
<span data-ttu-id="a125e-117">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="a125e-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a125e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a125e-118">-ResourceId</span></span>
<span data-ttu-id="a125e-119">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="a125e-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a125e-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a125e-120">-VaultName</span></span>
<span data-ttu-id="a125e-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a125e-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a125e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a125e-122">CommonParameters</span></span>
<span data-ttu-id="a125e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a125e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a125e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a125e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a125e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a125e-125">INPUTS</span></span>

### <span data-ttu-id="a125e-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a125e-126">None</span></span>
<span data-ttu-id="a125e-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a125e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a125e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a125e-128">OUTPUTS</span></span>

### <span data-ttu-id="a125e-129">Lista<Microsoft. Azure. Commands.. models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="a125e-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="a125e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a125e-130">NOTES</span></span>

## <span data-ttu-id="a125e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a125e-131">RELATED LINKS</span></span>

[<span data-ttu-id="a125e-132">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a125e-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="a125e-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a125e-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

