---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 19e443a4e7bca12a988e3a339fe9d568d81431b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550603"
---
# <span data-ttu-id="76075-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="76075-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="76075-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76075-102">SYNOPSIS</span></span>
<span data-ttu-id="76075-103">Pobiera właściwości kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="76075-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76075-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76075-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76075-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76075-105">DESCRIPTION</span></span>
<span data-ttu-id="76075-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupProperty** pobiera właściwości kopii zapasowej magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="76075-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="76075-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76075-107">EXAMPLES</span></span>

### <span data-ttu-id="76075-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76075-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="76075-109">Pobierz Właściwość magazyn kopii zapasowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="76075-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="76075-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76075-110">PARAMETERS</span></span>

### <span data-ttu-id="76075-111">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="76075-111">-Vault</span></span>
<span data-ttu-id="76075-112">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="76075-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="76075-113">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="76075-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76075-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76075-114">-DefaultProfile</span></span>
<span data-ttu-id="76075-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76075-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76075-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76075-116">CommonParameters</span></span>
<span data-ttu-id="76075-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76075-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76075-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76075-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76075-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76075-119">INPUTS</span></span>

### <span data-ttu-id="76075-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="76075-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="76075-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76075-121">OUTPUTS</span></span>

### <span data-ttu-id="76075-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="76075-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="76075-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76075-123">NOTES</span></span>

## <span data-ttu-id="76075-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76075-124">RELATED LINKS</span></span>

