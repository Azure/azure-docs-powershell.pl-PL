---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062691"
---
# <span data-ttu-id="e42cb-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e42cb-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e42cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e42cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e42cb-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e42cb-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="e42cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e42cb-104">SYNTAX</span></span>

### <span data-ttu-id="e42cb-105">Magazynname (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e42cb-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e42cb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e42cb-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e42cb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e42cb-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e42cb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e42cb-108">DESCRIPTION</span></span>
<span data-ttu-id="e42cb-109">Polecenie cmdlet **Get-AzKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="e42cb-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e42cb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e42cb-110">EXAMPLES</span></span>

### <span data-ttu-id="e42cb-111">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="e42cb-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="e42cb-112">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="e42cb-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="e42cb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e42cb-113">PARAMETERS</span></span>

### <span data-ttu-id="e42cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42cb-114">-DefaultProfile</span></span>
<span data-ttu-id="e42cb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e42cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e42cb-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e42cb-116">-InputObject</span></span>
<span data-ttu-id="e42cb-117">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="e42cb-117">KeyVault object.</span></span>

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

### <span data-ttu-id="e42cb-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e42cb-118">-ResourceId</span></span>
<span data-ttu-id="e42cb-119">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="e42cb-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="e42cb-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e42cb-120">-VaultName</span></span>
<span data-ttu-id="e42cb-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e42cb-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e42cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42cb-122">CommonParameters</span></span>
<span data-ttu-id="e42cb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42cb-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e42cb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42cb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42cb-125">INPUTS</span></span>

### <span data-ttu-id="e42cb-126">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e42cb-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e42cb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e42cb-127">System.String</span></span>

## <span data-ttu-id="e42cb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e42cb-128">OUTPUTS</span></span>

### <span data-ttu-id="e42cb-129">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e42cb-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e42cb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e42cb-130">NOTES</span></span>

## <span data-ttu-id="e42cb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e42cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="e42cb-132">Dodaj-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e42cb-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e42cb-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e42cb-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

