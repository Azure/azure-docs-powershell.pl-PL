---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543875"
---
# <span data-ttu-id="c6baa-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="c6baa-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="c6baa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6baa-102">SYNOPSIS</span></span>
<span data-ttu-id="c6baa-103">Pobiera zasady automatycznego uruchamiania laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="c6baa-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6baa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6baa-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6baa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6baa-105">DESCRIPTION</span></span>
<span data-ttu-id="c6baa-106">Polecenie cmdlet **Get-AzureRmDtlAutoStartPolicy** pobiera zasady automatycznego uruchamiania laboratorium, które planuje maszyny wirtualne laboratorium w celu automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="c6baa-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="c6baa-107">Polecenie cmdlet zwraca stan włączenia lub wyłączenia zasad oraz dni tygodnia i godziny, które ustawiono, aby umożliwić maszynom wirtualnym laboratorium planowanie automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="c6baa-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="c6baa-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6baa-108">EXAMPLES</span></span>

## <span data-ttu-id="c6baa-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6baa-109">PARAMETERS</span></span>

### <span data-ttu-id="c6baa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6baa-110">-DefaultProfile</span></span>
<span data-ttu-id="c6baa-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c6baa-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6baa-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c6baa-112">-LabName</span></span>
<span data-ttu-id="c6baa-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="c6baa-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6baa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6baa-114">-ResourceGroupName</span></span>
<span data-ttu-id="c6baa-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="c6baa-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6baa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6baa-116">CommonParameters</span></span>
<span data-ttu-id="c6baa-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6baa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6baa-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6baa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6baa-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6baa-119">INPUTS</span></span>

### <span data-ttu-id="c6baa-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c6baa-120">System.String</span></span>

## <span data-ttu-id="c6baa-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6baa-121">OUTPUTS</span></span>

### <span data-ttu-id="c6baa-122">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c6baa-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="c6baa-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6baa-123">NOTES</span></span>

## <span data-ttu-id="c6baa-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6baa-124">RELATED LINKS</span></span>

[<span data-ttu-id="c6baa-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="c6baa-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)

