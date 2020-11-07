---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718323"
---
# <span data-ttu-id="7aed7-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7aed7-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7aed7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7aed7-102">SYNOPSIS</span></span>
<span data-ttu-id="7aed7-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7aed7-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aed7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7aed7-104">SYNTAX</span></span>

### <span data-ttu-id="7aed7-105">Magazynname (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7aed7-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aed7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7aed7-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aed7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7aed7-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aed7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7aed7-108">DESCRIPTION</span></span>
<span data-ttu-id="7aed7-109">Polecenie cmdlet **Get-AzureKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="7aed7-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7aed7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7aed7-110">EXAMPLES</span></span>

### <span data-ttu-id="7aed7-111">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="7aed7-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="7aed7-112">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="7aed7-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="7aed7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7aed7-113">PARAMETERS</span></span>

### <span data-ttu-id="7aed7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aed7-114">-DefaultProfile</span></span>
<span data-ttu-id="7aed7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7aed7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7aed7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7aed7-116">-InputObject</span></span>
<span data-ttu-id="7aed7-117">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="7aed7-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7aed7-118">-ResourceId</span></span>
<span data-ttu-id="7aed7-119">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="7aed7-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed7-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="7aed7-120">-VaultName</span></span>
<span data-ttu-id="7aed7-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7aed7-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aed7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aed7-122">CommonParameters</span></span>
<span data-ttu-id="7aed7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aed7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aed7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aed7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aed7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7aed7-125">INPUTS</span></span>

### <span data-ttu-id="7aed7-126">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7aed7-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="7aed7-127">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7aed7-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7aed7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7aed7-128">System.String</span></span>

## <span data-ttu-id="7aed7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7aed7-129">OUTPUTS</span></span>

### <span data-ttu-id="7aed7-130">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7aed7-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7aed7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7aed7-131">NOTES</span></span>

## <span data-ttu-id="7aed7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7aed7-132">RELATED LINKS</span></span>

[<span data-ttu-id="7aed7-133">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7aed7-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="7aed7-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7aed7-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

