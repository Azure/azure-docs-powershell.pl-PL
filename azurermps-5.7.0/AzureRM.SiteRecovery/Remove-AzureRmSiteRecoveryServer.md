---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718430"
---
# <span data-ttu-id="25547-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="25547-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="25547-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25547-102">SYNOPSIS</span></span>
<span data-ttu-id="25547-103">Usuwa serwer odzyskiwania witryny z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="25547-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25547-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25547-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25547-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25547-105">DESCRIPTION</span></span>
<span data-ttu-id="25547-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryServer** umożliwia Wyrejestrowanie serwera odzyskiwania witryny platformy Azure, który usuwa go z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="25547-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="25547-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25547-107">EXAMPLES</span></span>

## <span data-ttu-id="25547-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25547-108">PARAMETERS</span></span>

### <span data-ttu-id="25547-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25547-109">-DefaultProfile</span></span>
<span data-ttu-id="25547-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25547-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25547-111">-Force</span><span class="sxs-lookup"><span data-stu-id="25547-111">-Force</span></span>
<span data-ttu-id="25547-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25547-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25547-113">-Server</span><span class="sxs-lookup"><span data-stu-id="25547-113">-Server</span></span>
<span data-ttu-id="25547-114">Określa obiekt serwera odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="25547-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25547-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25547-115">-Confirm</span></span>
<span data-ttu-id="25547-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25547-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25547-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25547-117">-WhatIf</span></span>
<span data-ttu-id="25547-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25547-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="25547-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25547-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25547-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25547-120">CommonParameters</span></span>
<span data-ttu-id="25547-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25547-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25547-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25547-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25547-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25547-123">INPUTS</span></span>

### <span data-ttu-id="25547-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="25547-124">ASRServer</span></span>
<span data-ttu-id="25547-125">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="25547-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="25547-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25547-126">OUTPUTS</span></span>

### <span data-ttu-id="25547-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="25547-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="25547-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25547-128">NOTES</span></span>

## <span data-ttu-id="25547-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25547-129">RELATED LINKS</span></span>

[<span data-ttu-id="25547-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="25547-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="25547-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="25547-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
