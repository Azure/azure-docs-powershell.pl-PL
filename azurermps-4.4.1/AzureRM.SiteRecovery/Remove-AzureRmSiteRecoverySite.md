---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717786"
---
# <span data-ttu-id="6fc61-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6fc61-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="6fc61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fc61-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc61-103">Usuwa witrynę odzyskiwania witryny z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fc61-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fc61-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fc61-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc61-106">Polecenie cmdlet **Remove-AzureRmSiteRecoverySite** usuwa witrynę Azure Site Recovery z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fc61-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="6fc61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fc61-107">EXAMPLES</span></span>

## <span data-ttu-id="6fc61-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fc61-108">PARAMETERS</span></span>

### <span data-ttu-id="6fc61-109">-Force</span><span class="sxs-lookup"><span data-stu-id="6fc61-109">-Force</span></span>
<span data-ttu-id="6fc61-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fc61-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc61-111">-Site</span><span class="sxs-lookup"><span data-stu-id="6fc61-111">-Site</span></span>
<span data-ttu-id="6fc61-112">Określa obiekt witryny odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6fc61-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc61-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fc61-113">-Confirm</span></span>
<span data-ttu-id="6fc61-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc61-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc61-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc61-115">-WhatIf</span></span>
<span data-ttu-id="6fc61-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc61-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6fc61-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6fc61-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc61-118">-DefaultProfile</span></span>
<span data-ttu-id="6fc61-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc61-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc61-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc61-120">CommonParameters</span></span>
<span data-ttu-id="6fc61-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc61-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc61-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc61-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc61-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fc61-123">INPUTS</span></span>

### <span data-ttu-id="6fc61-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="6fc61-124">ASRSite</span></span>
<span data-ttu-id="6fc61-125">Parametr "Witryna" przyjmuje wartość typu "ASRSite" z potoku.</span><span class="sxs-lookup"><span data-stu-id="6fc61-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="6fc61-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fc61-126">OUTPUTS</span></span>

## <span data-ttu-id="6fc61-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fc61-127">NOTES</span></span>

## <span data-ttu-id="6fc61-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fc61-128">RELATED LINKS</span></span>

[<span data-ttu-id="6fc61-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6fc61-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="6fc61-130">Nowe — AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="6fc61-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
