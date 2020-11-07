---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719237"
---
# <span data-ttu-id="c093a-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="c093a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c093a-102">SYNOPSIS</span></span>
<span data-ttu-id="c093a-103">Aktualizuje plan odzyskiwania w witrynie odzyskiwanie witryny.</span><span class="sxs-lookup"><span data-stu-id="c093a-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c093a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c093a-104">SYNTAX</span></span>

### <span data-ttu-id="c093a-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c093a-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c093a-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="c093a-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c093a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c093a-107">DESCRIPTION</span></span>
<span data-ttu-id="c093a-108">Polecenie cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** aktualizuje plan odzyskiwania w usłudze Azure Site Recovery, a następnie go publikuje.</span><span class="sxs-lookup"><span data-stu-id="c093a-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="c093a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c093a-109">EXAMPLES</span></span>

### <span data-ttu-id="c093a-110">Przykład 1: aktualizowanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="c093a-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="c093a-111">To polecenie powoduje zaktualizowanie określonego planu odzyskiwania, a następnie jego opublikowanie.</span><span class="sxs-lookup"><span data-stu-id="c093a-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="c093a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c093a-112">PARAMETERS</span></span>

### <span data-ttu-id="c093a-113">-Path</span><span class="sxs-lookup"><span data-stu-id="c093a-113">-Path</span></span>
<span data-ttu-id="c093a-114">Określa ścieżkę pliku planu odzyskiwania planu odzyskiwania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c093a-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c093a-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-115">-RecoveryPlan</span></span>
<span data-ttu-id="c093a-116">Określa plan odzyskiwania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c093a-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c093a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c093a-117">-DefaultProfile</span></span>
<span data-ttu-id="c093a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c093a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c093a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c093a-119">CommonParameters</span></span>
<span data-ttu-id="c093a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c093a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c093a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c093a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c093a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c093a-122">INPUTS</span></span>

### <span data-ttu-id="c093a-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="c093a-124">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c093a-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="c093a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c093a-125">OUTPUTS</span></span>

## <span data-ttu-id="c093a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c093a-126">NOTES</span></span>

## <span data-ttu-id="c093a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c093a-127">RELATED LINKS</span></span>

[<span data-ttu-id="c093a-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c093a-129">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c093a-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c093a-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


