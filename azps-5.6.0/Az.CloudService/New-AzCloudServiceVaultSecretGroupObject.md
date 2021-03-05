---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994491"
---
# <span data-ttu-id="8a466-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="8a466-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="8a466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a466-102">SYNOPSIS</span></span>
<span data-ttu-id="8a466-103">Tworzenie obiektu w pamięci dla grupy tajnej magazynu</span><span class="sxs-lookup"><span data-stu-id="8a466-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="8a466-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a466-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a466-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a466-105">DESCRIPTION</span></span>
<span data-ttu-id="8a466-106">Tworzenie obiektu w pamięci dla grupy tajnej</span><span class="sxs-lookup"><span data-stu-id="8a466-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="8a466-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a466-107">EXAMPLES</span></span>

### <span data-ttu-id="8a466-108">Przykład 1. Tworzenie obiektu grupy tajnej magazynu</span><span class="sxs-lookup"><span data-stu-id="8a466-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="8a466-109">To polecenie tworzy obiekt grupy tajnej magazynu, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="8a466-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="8a466-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="8a466-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="8a466-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a466-111">PARAMETERS</span></span>

### <span data-ttu-id="8a466-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="8a466-112">-CertificateUrl</span></span>
<span data-ttu-id="8a466-113">Jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="8a466-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

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

### <span data-ttu-id="8a466-114">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="8a466-114">-Id</span></span>
<span data-ttu-id="8a466-115">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8a466-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="8a466-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a466-116">CommonParameters</span></span>
<span data-ttu-id="8a466-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a466-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a466-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a466-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a466-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a466-119">INPUTS</span></span>

## <span data-ttu-id="8a466-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a466-120">OUTPUTS</span></span>

### <span data-ttu-id="8a466-121">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="8a466-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="8a466-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a466-122">NOTES</span></span>

<span data-ttu-id="8a466-123">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8a466-123">ALIASES</span></span>

## <span data-ttu-id="8a466-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a466-124">RELATED LINKS</span></span>

