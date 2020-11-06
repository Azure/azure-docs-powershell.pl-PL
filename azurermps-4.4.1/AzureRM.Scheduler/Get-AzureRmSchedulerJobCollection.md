---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553762"
---
# <span data-ttu-id="51815-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="51815-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51815-102">SYNOPSIS</span></span>
<span data-ttu-id="51815-103">Pobiera kolekcje zadań.</span><span class="sxs-lookup"><span data-stu-id="51815-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51815-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51815-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51815-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51815-105">DESCRIPTION</span></span>
<span data-ttu-id="51815-106">Polecenie cmdlet **Get-AzureRmSchedulerJobCollection** pobiera kolekcje zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="51815-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="51815-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51815-107">EXAMPLES</span></span>

## <span data-ttu-id="51815-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51815-108">PARAMETERS</span></span>

### <span data-ttu-id="51815-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="51815-109">-JobCollectionName</span></span>
<span data-ttu-id="51815-110">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="51815-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51815-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51815-111">-ResourceGroupName</span></span>
<span data-ttu-id="51815-112">Określa grupę zasobów, z której to polecenie cmdlet pobiera kolekcje zadań.</span><span class="sxs-lookup"><span data-stu-id="51815-112">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51815-113">-DefaultProfile</span></span>
<span data-ttu-id="51815-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51815-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51815-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51815-115">CommonParameters</span></span>
<span data-ttu-id="51815-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51815-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51815-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51815-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51815-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51815-118">INPUTS</span></span>

## <span data-ttu-id="51815-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51815-119">OUTPUTS</span></span>

### <span data-ttu-id="51815-120">System. Object</span><span class="sxs-lookup"><span data-stu-id="51815-120">System.Object</span></span>

## <span data-ttu-id="51815-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51815-121">NOTES</span></span>

## <span data-ttu-id="51815-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51815-122">RELATED LINKS</span></span>

[<span data-ttu-id="51815-123">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-123">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51815-124">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-124">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51815-125">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-125">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51815-126">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-126">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="51815-127">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="51815-127">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


