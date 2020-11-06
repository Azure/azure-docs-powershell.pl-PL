---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549543"
---
# <span data-ttu-id="40030-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="40030-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="40030-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40030-102">SYNOPSIS</span></span>
<span data-ttu-id="40030-103">Aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="40030-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40030-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40030-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40030-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40030-105">DESCRIPTION</span></span>
<span data-ttu-id="40030-106">Polecenie cmdlet **Update-AzureRmSiteRecoveryServicesProvider** aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="40030-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="40030-107">Za pomocą tego polecenia cmdlet można wyzwolić odświeżenie informacji otrzymanych od dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="40030-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="40030-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40030-108">EXAMPLES</span></span>

## <span data-ttu-id="40030-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40030-109">PARAMETERS</span></span>

### <span data-ttu-id="40030-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40030-110">-DefaultProfile</span></span>
<span data-ttu-id="40030-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40030-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40030-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="40030-112">-ServicesProvider</span></span>
<span data-ttu-id="40030-113">Określa obiekt dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="40030-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40030-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40030-114">CommonParameters</span></span>
<span data-ttu-id="40030-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40030-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40030-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40030-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40030-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40030-117">INPUTS</span></span>

### <span data-ttu-id="40030-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="40030-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="40030-119">Parametr "ServicesProvider" akceptuje wartość typu "ASRRecoveryServicesProvider" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="40030-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="40030-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40030-120">OUTPUTS</span></span>

## <span data-ttu-id="40030-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40030-121">NOTES</span></span>

## <span data-ttu-id="40030-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40030-122">RELATED LINKS</span></span>

[<span data-ttu-id="40030-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="40030-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="40030-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="40030-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
