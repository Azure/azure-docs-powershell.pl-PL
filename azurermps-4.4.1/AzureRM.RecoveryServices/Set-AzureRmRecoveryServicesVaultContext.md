---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718720"
---
# <span data-ttu-id="0cd63-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="0cd63-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="0cd63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cd63-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd63-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="0cd63-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cd63-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0cd63-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd63-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd63-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="0cd63-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cd63-107">EXAMPLES</span></span>

## <span data-ttu-id="0cd63-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cd63-108">PARAMETERS</span></span>

### <span data-ttu-id="0cd63-109">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="0cd63-109">-Vault</span></span>
<span data-ttu-id="0cd63-110">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="0cd63-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="0cd63-111">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="0cd63-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="0cd63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd63-112">-DefaultProfile</span></span>
<span data-ttu-id="0cd63-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd63-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cd63-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd63-114">CommonParameters</span></span>
<span data-ttu-id="0cd63-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd63-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd63-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd63-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd63-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cd63-117">INPUTS</span></span>

### <span data-ttu-id="0cd63-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="0cd63-118">ARSVault</span></span>
<span data-ttu-id="0cd63-119">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="0cd63-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="0cd63-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cd63-120">OUTPUTS</span></span>

## <span data-ttu-id="0cd63-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cd63-121">NOTES</span></span>

## <span data-ttu-id="0cd63-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cd63-122">RELATED LINKS</span></span>

