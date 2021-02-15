---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200738"
---
# <span data-ttu-id="de70d-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="de70d-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="de70d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de70d-102">SYNOPSIS</span></span>
<span data-ttu-id="de70d-103">Tworzenie obiektu w pamięci dla grupy tajnej magazynu</span><span class="sxs-lookup"><span data-stu-id="de70d-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="de70d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de70d-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="de70d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de70d-105">DESCRIPTION</span></span>
<span data-ttu-id="de70d-106">Tworzenie obiektu w pamięci dla grupy tajnej</span><span class="sxs-lookup"><span data-stu-id="de70d-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="de70d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de70d-107">EXAMPLES</span></span>

### <span data-ttu-id="de70d-108">Przykład 1. Tworzenie obiektu grupy tajnej magazynu</span><span class="sxs-lookup"><span data-stu-id="de70d-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="de70d-109">To polecenie tworzy obiekt grupy tajnej magazynu, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="de70d-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="de70d-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="de70d-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="de70d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de70d-111">PARAMETERS</span></span>

### <span data-ttu-id="de70d-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="de70d-112">-CertificateUrl</span></span>
<span data-ttu-id="de70d-113">Jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="de70d-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de70d-114">— Id</span><span class="sxs-lookup"><span data-stu-id="de70d-114">-Id</span></span>
<span data-ttu-id="de70d-115">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="de70d-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de70d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de70d-116">CommonParameters</span></span>
<span data-ttu-id="de70d-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de70d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de70d-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de70d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de70d-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de70d-119">INPUTS</span></span>

## <span data-ttu-id="de70d-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de70d-120">OUTPUTS</span></span>

### <span data-ttu-id="de70d-121">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="de70d-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="de70d-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de70d-122">NOTES</span></span>

<span data-ttu-id="de70d-123">ALIASY</span><span class="sxs-lookup"><span data-stu-id="de70d-123">ALIASES</span></span>

## <span data-ttu-id="de70d-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de70d-124">RELATED LINKS</span></span>

