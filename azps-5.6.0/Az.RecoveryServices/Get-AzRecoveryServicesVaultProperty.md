---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973642"
---
# <span data-ttu-id="470f2-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="470f2-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="470f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470f2-102">SYNOPSIS</span></span>
<span data-ttu-id="470f2-103">Zwraca właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="470f2-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="470f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="470f2-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="470f2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="470f2-105">DESCRIPTION</span></span>
<span data-ttu-id="470f2-106">Polecenie **cmdlet Get-AzRecoveryServicesVaultProperty** zwraca właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="470f2-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="470f2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="470f2-107">EXAMPLES</span></span>

### <span data-ttu-id="470f2-108">Przykład 1. Uzyskiwanie właściwości magazynu</span><span class="sxs-lookup"><span data-stu-id="470f2-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="470f2-109">Pierwsze polecenie pobiera obiekt magazynu, a następnie przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="470f2-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="470f2-110">Drugie polecenie pobiera właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="470f2-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="470f2-111">Następnie uzyskujemy dostęp do właściwości szyfrowania magazynu.</span><span class="sxs-lookup"><span data-stu-id="470f2-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="470f2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="470f2-112">PARAMETERS</span></span>

### <span data-ttu-id="470f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470f2-113">-DefaultProfile</span></span>
<span data-ttu-id="470f2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="470f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470f2-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="470f2-115">-VaultId</span></span>
<span data-ttu-id="470f2-116">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="470f2-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470f2-117">CommonParameters</span></span>
<span data-ttu-id="470f2-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470f2-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="470f2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470f2-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="470f2-120">INPUTS</span></span>

### <span data-ttu-id="470f2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="470f2-121">System.String</span></span>

## <span data-ttu-id="470f2-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="470f2-122">OUTPUTS</span></span>

### <span data-ttu-id="470f2-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="470f2-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="470f2-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="470f2-124">NOTES</span></span>

## <span data-ttu-id="470f2-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="470f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="470f2-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="470f2-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="470f2-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="470f2-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
