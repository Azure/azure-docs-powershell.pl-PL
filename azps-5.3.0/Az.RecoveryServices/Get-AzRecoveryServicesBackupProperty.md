---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498550"
---
# <span data-ttu-id="34770-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="34770-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="34770-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34770-102">SYNOPSIS</span></span>
<span data-ttu-id="34770-103">Pobiera właściwości kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="34770-103">Gets Backup properties.</span></span>

## <span data-ttu-id="34770-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34770-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34770-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34770-105">DESCRIPTION</span></span>
<span data-ttu-id="34770-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupProperty** pobiera właściwości kopii zapasowej magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="34770-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="34770-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34770-107">EXAMPLES</span></span>

### <span data-ttu-id="34770-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34770-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="34770-109">Pobierz Właściwość magazyn kopii zapasowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="34770-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="34770-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34770-110">PARAMETERS</span></span>

### <span data-ttu-id="34770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34770-111">-DefaultProfile</span></span>
<span data-ttu-id="34770-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34770-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34770-113">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="34770-113">-Vault</span></span>
<span data-ttu-id="34770-114">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="34770-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="34770-115">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="34770-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="34770-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34770-116">CommonParameters</span></span>
<span data-ttu-id="34770-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34770-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34770-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34770-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34770-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34770-119">INPUTS</span></span>

### <span data-ttu-id="34770-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="34770-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="34770-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34770-121">OUTPUTS</span></span>

### <span data-ttu-id="34770-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="34770-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="34770-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34770-123">NOTES</span></span>

## <span data-ttu-id="34770-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34770-124">RELATED LINKS</span></span>
