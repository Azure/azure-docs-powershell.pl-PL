---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192923"
---
# <span data-ttu-id="a0e33-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a0e33-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="a0e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0e33-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e33-103">Zwraca właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a0e33-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="a0e33-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0e33-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e33-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0e33-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e33-106">Polecenie **cmdlet Get-AzRecoveryServicesVaultProperty** zwraca właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a0e33-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="a0e33-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0e33-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e33-108">Przykład 1. Uzyskiwanie właściwości magazynu</span><span class="sxs-lookup"><span data-stu-id="a0e33-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="a0e33-109">Pierwsze polecenie pobiera obiekt magazynu, a następnie przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="a0e33-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="a0e33-110">Drugie polecenie pobiera właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0e33-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="a0e33-111">Następnie uzyskujemy dostęp do właściwości szyfrowania magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0e33-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="a0e33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0e33-112">PARAMETERS</span></span>

### <span data-ttu-id="a0e33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e33-113">-DefaultProfile</span></span>
<span data-ttu-id="a0e33-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e33-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e33-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a0e33-115">-VaultId</span></span>
<span data-ttu-id="a0e33-116">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a0e33-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a0e33-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e33-117">CommonParameters</span></span>
<span data-ttu-id="a0e33-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e33-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e33-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0e33-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e33-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0e33-120">INPUTS</span></span>

### <span data-ttu-id="a0e33-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a0e33-121">System.String</span></span>

## <span data-ttu-id="a0e33-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0e33-122">OUTPUTS</span></span>

### <span data-ttu-id="a0e33-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="a0e33-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="a0e33-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0e33-124">NOTES</span></span>

## <span data-ttu-id="a0e33-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0e33-125">RELATED LINKS</span></span>

[<span data-ttu-id="a0e33-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a0e33-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a0e33-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a0e33-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
