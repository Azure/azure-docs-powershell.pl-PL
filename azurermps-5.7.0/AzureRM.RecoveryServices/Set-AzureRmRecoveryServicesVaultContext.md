---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717714"
---
# <span data-ttu-id="9cdfd-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9cdfd-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9cdfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdfd-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cdfd-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cdfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cdfd-105">DESCRIPTION</span></span>
<span data-ttu-id="9cdfd-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="9cdfd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cdfd-107">EXAMPLES</span></span>

### <span data-ttu-id="9cdfd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cdfd-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9cdfd-109">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-109">Sets vault context.</span></span>

## <span data-ttu-id="9cdfd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cdfd-110">PARAMETERS</span></span>

### <span data-ttu-id="9cdfd-111">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="9cdfd-111">-Vault</span></span>
<span data-ttu-id="9cdfd-112">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="9cdfd-113">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="9cdfd-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9cdfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdfd-114">-DefaultProfile</span></span>
<span data-ttu-id="9cdfd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cdfd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdfd-116">CommonParameters</span></span>
<span data-ttu-id="9cdfd-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdfd-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdfd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdfd-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cdfd-119">INPUTS</span></span>

### <span data-ttu-id="9cdfd-120">ARSVault</span><span class="sxs-lookup"><span data-stu-id="9cdfd-120">ARSVault</span></span>
<span data-ttu-id="9cdfd-121">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="9cdfd-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="9cdfd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cdfd-122">OUTPUTS</span></span>

## <span data-ttu-id="9cdfd-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cdfd-123">NOTES</span></span>

## <span data-ttu-id="9cdfd-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cdfd-124">RELATED LINKS</span></span>

