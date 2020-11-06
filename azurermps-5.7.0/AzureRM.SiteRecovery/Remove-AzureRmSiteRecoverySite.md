---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524914"
---
# <span data-ttu-id="1d041-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="1d041-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="1d041-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d041-102">SYNOPSIS</span></span>
<span data-ttu-id="1d041-103">Usuwa witrynę odzyskiwania witryny z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="1d041-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d041-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d041-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d041-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d041-105">DESCRIPTION</span></span>
<span data-ttu-id="1d041-106">Polecenie cmdlet **Remove-AzureRmSiteRecoverySite** usuwa witrynę Azure Site Recovery z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="1d041-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="1d041-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d041-107">EXAMPLES</span></span>

## <span data-ttu-id="1d041-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d041-108">PARAMETERS</span></span>

### <span data-ttu-id="1d041-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d041-109">-DefaultProfile</span></span>
<span data-ttu-id="1d041-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d041-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d041-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1d041-111">-Force</span></span>
<span data-ttu-id="1d041-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1d041-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-113">-Site</span><span class="sxs-lookup"><span data-stu-id="1d041-113">-Site</span></span>
<span data-ttu-id="1d041-114">Określa obiekt witryny odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="1d041-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d041-115">-Confirm</span></span>
<span data-ttu-id="1d041-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d041-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d041-117">-WhatIf</span></span>
<span data-ttu-id="1d041-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d041-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1d041-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d041-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d041-120">CommonParameters</span></span>
<span data-ttu-id="1d041-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d041-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d041-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d041-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d041-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d041-123">INPUTS</span></span>

### <span data-ttu-id="1d041-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="1d041-124">ASRSite</span></span>
<span data-ttu-id="1d041-125">Parametr "Witryna" przyjmuje wartość typu "ASRSite" z potoku.</span><span class="sxs-lookup"><span data-stu-id="1d041-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="1d041-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d041-126">OUTPUTS</span></span>

## <span data-ttu-id="1d041-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d041-127">NOTES</span></span>

## <span data-ttu-id="1d041-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d041-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d041-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="1d041-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="1d041-130">Nowe — AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="1d041-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
