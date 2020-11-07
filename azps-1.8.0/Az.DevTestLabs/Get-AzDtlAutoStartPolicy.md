---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 449206713291499c344975e490c3b0d89ab1d88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709915"
---
# <span data-ttu-id="be248-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="be248-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="be248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be248-102">SYNOPSIS</span></span>
<span data-ttu-id="be248-103">Pobiera zasady automatycznego uruchamiania laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="be248-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="be248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be248-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be248-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be248-105">DESCRIPTION</span></span>
<span data-ttu-id="be248-106">Polecenie cmdlet **Get-AzDtlAutoStartPolicy** pobiera zasady automatycznego uruchamiania laboratorium, które planuje maszyny wirtualne laboratorium w celu automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="be248-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="be248-107">Polecenie cmdlet zwraca stan włączenia lub wyłączenia zasad oraz dni tygodnia i godziny, które ustawiono, aby umożliwić maszynom wirtualnym laboratorium planowanie automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="be248-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="be248-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be248-108">EXAMPLES</span></span>

## <span data-ttu-id="be248-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be248-109">PARAMETERS</span></span>

### <span data-ttu-id="be248-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be248-110">-DefaultProfile</span></span>
<span data-ttu-id="be248-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="be248-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be248-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="be248-112">-LabName</span></span>
<span data-ttu-id="be248-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady automatycznego uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="be248-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="be248-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be248-114">-ResourceGroupName</span></span>
<span data-ttu-id="be248-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="be248-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="be248-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be248-116">CommonParameters</span></span>
<span data-ttu-id="be248-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be248-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be248-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be248-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be248-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be248-119">INPUTS</span></span>

### <span data-ttu-id="be248-120">System. String</span><span class="sxs-lookup"><span data-stu-id="be248-120">System.String</span></span>

## <span data-ttu-id="be248-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be248-121">OUTPUTS</span></span>

### <span data-ttu-id="be248-122">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="be248-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="be248-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be248-123">NOTES</span></span>

## <span data-ttu-id="be248-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be248-124">RELATED LINKS</span></span>

[<span data-ttu-id="be248-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="be248-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


