---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719238"
---
# <span data-ttu-id="23aa1-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="23aa1-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="23aa1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="23aa1-103">Usuwa serwer odzyskiwania witryny z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="23aa1-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23aa1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23aa1-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23aa1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="23aa1-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryServer** umożliwia Wyrejestrowanie serwera odzyskiwania witryny platformy Azure, który usuwa go z bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="23aa1-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="23aa1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23aa1-107">EXAMPLES</span></span>

## <span data-ttu-id="23aa1-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23aa1-108">PARAMETERS</span></span>

### <span data-ttu-id="23aa1-109">-Force</span><span class="sxs-lookup"><span data-stu-id="23aa1-109">-Force</span></span>
<span data-ttu-id="23aa1-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="23aa1-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23aa1-111">-Server</span><span class="sxs-lookup"><span data-stu-id="23aa1-111">-Server</span></span>
<span data-ttu-id="23aa1-112">Określa obiekt serwera odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="23aa1-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23aa1-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23aa1-113">-Confirm</span></span>
<span data-ttu-id="23aa1-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23aa1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23aa1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23aa1-115">-WhatIf</span></span>
<span data-ttu-id="23aa1-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23aa1-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="23aa1-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23aa1-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23aa1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23aa1-118">-DefaultProfile</span></span>
<span data-ttu-id="23aa1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23aa1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23aa1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23aa1-120">CommonParameters</span></span>
<span data-ttu-id="23aa1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23aa1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23aa1-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23aa1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23aa1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23aa1-123">INPUTS</span></span>

### <span data-ttu-id="23aa1-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="23aa1-124">ASRServer</span></span>
<span data-ttu-id="23aa1-125">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="23aa1-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="23aa1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23aa1-126">OUTPUTS</span></span>

### <span data-ttu-id="23aa1-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="23aa1-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="23aa1-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23aa1-128">NOTES</span></span>

## <span data-ttu-id="23aa1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23aa1-129">RELATED LINKS</span></span>

[<span data-ttu-id="23aa1-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="23aa1-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="23aa1-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="23aa1-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
