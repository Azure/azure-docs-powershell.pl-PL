---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984209"
---
# <span data-ttu-id="45e8f-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="45e8f-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="45e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="45e8f-103">Pobiera właściwości kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="45e8f-103">Gets Backup properties.</span></span>

## <span data-ttu-id="45e8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45e8f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45e8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="45e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="45e8f-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupProperty** pobiera właściwości kopii zapasowej dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="45e8f-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="45e8f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="45e8f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45e8f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="45e8f-109">Uzyskaj właściwość magazynu kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="45e8f-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="45e8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e8f-110">PARAMETERS</span></span>

### <span data-ttu-id="45e8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e8f-111">-DefaultProfile</span></span>
<span data-ttu-id="45e8f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45e8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45e8f-113">— magazyn</span><span class="sxs-lookup"><span data-stu-id="45e8f-113">-Vault</span></span>
<span data-ttu-id="45e8f-114">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="45e8f-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="45e8f-115">Magazyn musi być obiektem **AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="45e8f-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45e8f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e8f-116">CommonParameters</span></span>
<span data-ttu-id="45e8f-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e8f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e8f-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45e8f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e8f-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45e8f-119">INPUTS</span></span>

### <span data-ttu-id="45e8f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="45e8f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="45e8f-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45e8f-121">OUTPUTS</span></span>

### <span data-ttu-id="45e8f-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="45e8f-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="45e8f-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45e8f-123">NOTES</span></span>

## <span data-ttu-id="45e8f-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45e8f-124">RELATED LINKS</span></span>
