---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708570"
---
# <span data-ttu-id="01364-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="01364-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="01364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01364-102">SYNOPSIS</span></span>
<span data-ttu-id="01364-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="01364-103">Sets vault context.</span></span>

## <span data-ttu-id="01364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01364-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01364-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01364-105">DESCRIPTION</span></span>
<span data-ttu-id="01364-106">Polecenie cmdlet **Set-AzRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01364-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="01364-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01364-107">EXAMPLES</span></span>

### <span data-ttu-id="01364-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01364-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="01364-109">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="01364-109">Sets vault context.</span></span>

## <span data-ttu-id="01364-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01364-110">PARAMETERS</span></span>

### <span data-ttu-id="01364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01364-111">-DefaultProfile</span></span>
<span data-ttu-id="01364-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01364-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01364-113">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="01364-113">-Vault</span></span>
<span data-ttu-id="01364-114">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="01364-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="01364-115">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="01364-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="01364-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01364-116">CommonParameters</span></span>
<span data-ttu-id="01364-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01364-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01364-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01364-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01364-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01364-119">INPUTS</span></span>

### <span data-ttu-id="01364-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="01364-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="01364-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01364-121">OUTPUTS</span></span>

### <span data-ttu-id="01364-122">System. void</span><span class="sxs-lookup"><span data-stu-id="01364-122">System.Void</span></span>

## <span data-ttu-id="01364-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01364-123">NOTES</span></span>

## <span data-ttu-id="01364-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01364-124">RELATED LINKS</span></span>