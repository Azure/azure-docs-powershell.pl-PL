---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718112"
---
# <span data-ttu-id="bc646-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="bc646-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="bc646-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc646-102">SYNOPSIS</span></span>
<span data-ttu-id="bc646-103">Pobiera właściwości kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="bc646-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc646-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc646-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc646-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc646-105">DESCRIPTION</span></span>
<span data-ttu-id="bc646-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupProperty** pobiera właściwości kopii zapasowej magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="bc646-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="bc646-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc646-107">EXAMPLES</span></span>

## <span data-ttu-id="bc646-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc646-108">PARAMETERS</span></span>

### <span data-ttu-id="bc646-109">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="bc646-109">-Vault</span></span>
<span data-ttu-id="bc646-110">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="bc646-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="bc646-111">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="bc646-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="bc646-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc646-112">-DefaultProfile</span></span>
<span data-ttu-id="bc646-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc646-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc646-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc646-114">CommonParameters</span></span>
<span data-ttu-id="bc646-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc646-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc646-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc646-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc646-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc646-117">INPUTS</span></span>

### <span data-ttu-id="bc646-118">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="bc646-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="bc646-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc646-119">OUTPUTS</span></span>

### <span data-ttu-id="bc646-120">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="bc646-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="bc646-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc646-121">NOTES</span></span>

## <span data-ttu-id="bc646-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc646-122">RELATED LINKS</span></span>

