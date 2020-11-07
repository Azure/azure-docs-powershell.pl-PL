---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891318"
---
# <span data-ttu-id="9e9f2-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e9f2-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9e9f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9f2-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="9e9f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e9f2-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9f2-106">Polecenie cmdlet **Get-AzKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9e9f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="9e9f2-108">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="9e9f2-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="9e9f2-109">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="9e9f2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e9f2-110">PARAMETERS</span></span>

### <span data-ttu-id="9e9f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9f2-111">-DefaultProfile</span></span>
<span data-ttu-id="9e9f2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e9f2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e9f2-113">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9e9f2-113">-VaultName</span></span>
<span data-ttu-id="9e9f2-114">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="9e9f2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9f2-115">CommonParameters</span></span>
<span data-ttu-id="9e9f2-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9f2-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9f2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9f2-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e9f2-118">INPUTS</span></span>

### <span data-ttu-id="9e9f2-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e9f2-119">None</span></span>
<span data-ttu-id="9e9f2-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e9f2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e9f2-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e9f2-121">OUTPUTS</span></span>

### <span data-ttu-id="9e9f2-122">Lista<Microsoft. Azure. Commands.. models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="9e9f2-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="9e9f2-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e9f2-123">NOTES</span></span>

## <span data-ttu-id="9e9f2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e9f2-124">RELATED LINKS</span></span>

[<span data-ttu-id="9e9f2-125">Dodaj-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e9f2-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="9e9f2-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e9f2-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

