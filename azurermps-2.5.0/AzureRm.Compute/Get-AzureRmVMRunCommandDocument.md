---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898990"
---
# <span data-ttu-id="20299-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="20299-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="20299-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20299-102">SYNOPSIS</span></span>
<span data-ttu-id="20299-103">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="20299-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20299-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20299-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20299-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20299-105">DESCRIPTION</span></span>
<span data-ttu-id="20299-106">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="20299-106">Get run command document.</span></span>

## <span data-ttu-id="20299-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20299-107">EXAMPLES</span></span>

### <span data-ttu-id="20299-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20299-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="20299-109">Pobiera określony dokument polecenia Uruchom dla elementu "RunPowerShellScript" w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="20299-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="20299-110">Lokalizacja Get-AzureRmVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="20299-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="20299-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="20299-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="20299-112">Wyświetla wszystkie dostępne polecenia Uruchom w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="20299-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="20299-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20299-113">PARAMETERS</span></span>

### <span data-ttu-id="20299-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="20299-114">-CommandId</span></span>
<span data-ttu-id="20299-115">Identyfikator polecenia.</span><span class="sxs-lookup"><span data-stu-id="20299-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20299-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20299-116">-DefaultProfile</span></span>
<span data-ttu-id="20299-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20299-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20299-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="20299-118">-Location</span></span>
<span data-ttu-id="20299-119">Lokalizacja, w której są wysyłane zapytania dotyczące polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="20299-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20299-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20299-120">CommonParameters</span></span>
<span data-ttu-id="20299-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20299-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20299-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20299-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20299-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20299-123">INPUTS</span></span>

### <span data-ttu-id="20299-124">System. String</span><span class="sxs-lookup"><span data-stu-id="20299-124">System.String</span></span>

## <span data-ttu-id="20299-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20299-125">OUTPUTS</span></span>

### <span data-ttu-id="20299-126">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="20299-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="20299-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20299-127">NOTES</span></span>

## <span data-ttu-id="20299-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20299-128">RELATED LINKS</span></span>

