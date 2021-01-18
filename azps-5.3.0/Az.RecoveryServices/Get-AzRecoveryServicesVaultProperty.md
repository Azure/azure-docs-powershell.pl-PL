---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498546"
---
# <span data-ttu-id="aa6b3-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="aa6b3-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="aa6b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6b3-103">Zwraca właściwości magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="aa6b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa6b3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa6b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="aa6b3-106">Polecenie cmdlet **Get-AzRecoveryServicesVaultProperty** zwraca właściwości magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="aa6b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="aa6b3-108">Przykład 1: pobieranie właściwości magazynu</span><span class="sxs-lookup"><span data-stu-id="aa6b3-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="aa6b3-109">Pierwsze polecenie pobiera obiekt magazynu, a następnie zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="aa6b3-110">Drugie polecenie pobiera właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="aa6b3-111">Następna możemy uzyskać dostęp do encryptionProperties magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="aa6b3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa6b3-112">PARAMETERS</span></span>

### <span data-ttu-id="aa6b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6b3-113">-DefaultProfile</span></span>
<span data-ttu-id="aa6b3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa6b3-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="aa6b3-115">-VaultId</span></span>
<span data-ttu-id="aa6b3-116">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="aa6b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6b3-117">CommonParameters</span></span>
<span data-ttu-id="aa6b3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa6b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6b3-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa6b3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6b3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa6b3-120">INPUTS</span></span>

### <span data-ttu-id="aa6b3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="aa6b3-121">System.String</span></span>

## <span data-ttu-id="aa6b3-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa6b3-122">OUTPUTS</span></span>

### <span data-ttu-id="aa6b3-123">Microsoft. Azure. Management. RecoveryServices. Backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="aa6b3-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="aa6b3-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa6b3-124">NOTES</span></span>

## <span data-ttu-id="aa6b3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa6b3-125">RELATED LINKS</span></span>

[<span data-ttu-id="aa6b3-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="aa6b3-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="aa6b3-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="aa6b3-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
