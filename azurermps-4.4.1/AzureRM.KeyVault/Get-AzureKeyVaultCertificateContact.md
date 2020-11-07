---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718530"
---
# <span data-ttu-id="77f05-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="77f05-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="77f05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77f05-102">SYNOPSIS</span></span>
<span data-ttu-id="77f05-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="77f05-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77f05-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77f05-105">DESCRIPTION</span></span>
<span data-ttu-id="77f05-106">Polecenie cmdlet **Get-AzureKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="77f05-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="77f05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77f05-107">EXAMPLES</span></span>

### <span data-ttu-id="77f05-108">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="77f05-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="77f05-109">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="77f05-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="77f05-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77f05-110">PARAMETERS</span></span>

### <span data-ttu-id="77f05-111">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="77f05-111">-VaultName</span></span>
<span data-ttu-id="77f05-112">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="77f05-112">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f05-113">-DefaultProfile</span></span>
<span data-ttu-id="77f05-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77f05-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f05-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f05-115">CommonParameters</span></span>
<span data-ttu-id="77f05-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f05-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f05-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f05-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f05-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77f05-118">INPUTS</span></span>

## <span data-ttu-id="77f05-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77f05-119">OUTPUTS</span></span>

### <span data-ttu-id="77f05-120">Lista<Microsoft. Azure. Commands.. models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="77f05-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="77f05-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77f05-121">NOTES</span></span>

## <span data-ttu-id="77f05-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77f05-122">RELATED LINKS</span></span>

[<span data-ttu-id="77f05-123">Dodaj-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="77f05-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="77f05-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="77f05-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

