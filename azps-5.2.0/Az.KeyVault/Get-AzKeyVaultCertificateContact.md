---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323517"
---
# <span data-ttu-id="a06d6-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a06d6-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a06d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a06d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a06d6-103">Umożliwia wyświetlenie kontaktów zarejestrowanych w celu otrzymywania powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a06d6-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="a06d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a06d6-104">SYNTAX</span></span>

### <span data-ttu-id="a06d6-105">Magazynname (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a06d6-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a06d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a06d6-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a06d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a06d6-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a06d6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a06d6-108">DESCRIPTION</span></span>
<span data-ttu-id="a06d6-109">Polecenie cmdlet **Get-AzKeyVaultCertificateContact** umożliwia pobieranie kontaktów zarejestrowanych na potrzeby powiadamiania o certyfikatach dla magazynu kluczy w magazynie kluczy usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d6-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a06d6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a06d6-110">EXAMPLES</span></span>

### <span data-ttu-id="a06d6-111">Przykład 1: pobieranie wszystkich kontaktów z certyfikatem</span><span class="sxs-lookup"><span data-stu-id="a06d6-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="a06d6-112">To polecenie powoduje wyświetlenie wszystkich kontaktów dotyczących obiektów certyfikatu w magazynie kluczy contoso, a następnie zapisanie ich w zmiennej $Contacts.</span><span class="sxs-lookup"><span data-stu-id="a06d6-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="a06d6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a06d6-113">PARAMETERS</span></span>

### <span data-ttu-id="a06d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06d6-114">-DefaultProfile</span></span>
<span data-ttu-id="a06d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a06d6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a06d6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a06d6-116">-InputObject</span></span>
<span data-ttu-id="a06d6-117">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="a06d6-117">KeyVault object.</span></span>

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

### <span data-ttu-id="a06d6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a06d6-118">-ResourceId</span></span>
<span data-ttu-id="a06d6-119">Identyfikator magazynu.</span><span class="sxs-lookup"><span data-stu-id="a06d6-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="a06d6-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a06d6-120">-VaultName</span></span>
<span data-ttu-id="a06d6-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a06d6-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="a06d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06d6-122">CommonParameters</span></span>
<span data-ttu-id="a06d6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06d6-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a06d6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06d6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a06d6-125">INPUTS</span></span>

### <span data-ttu-id="a06d6-126">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a06d6-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a06d6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a06d6-127">System.String</span></span>

## <span data-ttu-id="a06d6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a06d6-128">OUTPUTS</span></span>

### <span data-ttu-id="a06d6-129">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a06d6-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a06d6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a06d6-130">NOTES</span></span>

## <span data-ttu-id="a06d6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a06d6-131">RELATED LINKS</span></span>

[<span data-ttu-id="a06d6-132">Dodaj-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a06d6-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="a06d6-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a06d6-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

