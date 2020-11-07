---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718083"
---
# <span data-ttu-id="12783-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="12783-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="12783-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12783-102">SYNOPSIS</span></span>
<span data-ttu-id="12783-103">Aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12783-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12783-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12783-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12783-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12783-105">DESCRIPTION</span></span>
<span data-ttu-id="12783-106">Polecenie cmdlet **Update-AzureRmSiteRecoveryServicesProvider** aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12783-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="12783-107">Za pomocą tego polecenia cmdlet można wyzwolić odświeżenie informacji otrzymanych od dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="12783-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="12783-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12783-108">EXAMPLES</span></span>

## <span data-ttu-id="12783-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12783-109">PARAMETERS</span></span>

### <span data-ttu-id="12783-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="12783-110">-ServicesProvider</span></span>
<span data-ttu-id="12783-111">Określa obiekt dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12783-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12783-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12783-112">-DefaultProfile</span></span>
<span data-ttu-id="12783-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12783-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12783-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12783-114">CommonParameters</span></span>
<span data-ttu-id="12783-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12783-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12783-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12783-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12783-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12783-117">INPUTS</span></span>

### <span data-ttu-id="12783-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="12783-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="12783-119">Parametr "ServicesProvider" akceptuje wartość typu "ASRRecoveryServicesProvider" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="12783-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="12783-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12783-120">OUTPUTS</span></span>

## <span data-ttu-id="12783-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12783-121">NOTES</span></span>

## <span data-ttu-id="12783-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12783-122">RELATED LINKS</span></span>

[<span data-ttu-id="12783-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="12783-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="12783-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="12783-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
