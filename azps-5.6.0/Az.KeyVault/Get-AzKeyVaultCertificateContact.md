---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 4a8eb9ce6fce4cf9719e365055cab5743d081b1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004042"
---
# <span data-ttu-id="e11a4-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e11a4-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e11a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e11a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e11a4-103">Pobiera kontakty zarejestrowane w celu powiadomień o certyfikatach dla magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e11a4-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="e11a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e11a4-104">SYNTAX</span></span>

### <span data-ttu-id="e11a4-105">Nazwa magazynu (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e11a4-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e11a4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e11a4-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e11a4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e11a4-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e11a4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e11a4-108">DESCRIPTION</span></span>
<span data-ttu-id="e11a4-109">Polecenie **cmdlet Get-AzKeyVaultCertificateContact** pobiera kontakty, które są zarejestrowane w celu powiadomień o certyfikatach dla magazynu kluczy w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e11a4-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e11a4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e11a4-110">EXAMPLES</span></span>

### <span data-ttu-id="e11a4-111">Przykład 1. Uzyskiwanie wszystkich kontaktów certyfikatów</span><span class="sxs-lookup"><span data-stu-id="e11a4-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="e11a4-112">To polecenie pobiera wszystkie kontakty dla obiektów certyfikatów w magazynie kluczy contoso, a następnie przechowuje je w $Contacts klucza.</span><span class="sxs-lookup"><span data-stu-id="e11a4-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="e11a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e11a4-113">PARAMETERS</span></span>

### <span data-ttu-id="e11a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e11a4-114">-DefaultProfile</span></span>
<span data-ttu-id="e11a4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e11a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e11a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e11a4-116">-InputObject</span></span>
<span data-ttu-id="e11a4-117">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e11a4-117">KeyVault object.</span></span>

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

### <span data-ttu-id="e11a4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e11a4-118">-ResourceId</span></span>
<span data-ttu-id="e11a4-119">Identyfikator KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e11a4-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="e11a4-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e11a4-120">-VaultName</span></span>
<span data-ttu-id="e11a4-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e11a4-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e11a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11a4-122">CommonParameters</span></span>
<span data-ttu-id="e11a4-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e11a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11a4-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e11a4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11a4-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e11a4-125">INPUTS</span></span>

### <span data-ttu-id="e11a4-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e11a4-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e11a4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e11a4-127">System.String</span></span>

## <span data-ttu-id="e11a4-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e11a4-128">OUTPUTS</span></span>

### <span data-ttu-id="e11a4-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e11a4-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e11a4-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e11a4-130">NOTES</span></span>

## <span data-ttu-id="e11a4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e11a4-131">RELATED LINKS</span></span>

[<span data-ttu-id="e11a4-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e11a4-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e11a4-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e11a4-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

