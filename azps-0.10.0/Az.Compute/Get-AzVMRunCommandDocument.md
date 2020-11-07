---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893725"
---
# <span data-ttu-id="0201c-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0201c-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="0201c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0201c-102">SYNOPSIS</span></span>
<span data-ttu-id="0201c-103">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="0201c-103">Get run command document.</span></span>

## <span data-ttu-id="0201c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0201c-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0201c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0201c-105">DESCRIPTION</span></span>
<span data-ttu-id="0201c-106">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="0201c-106">Get run command document.</span></span>

## <span data-ttu-id="0201c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0201c-107">EXAMPLES</span></span>

### <span data-ttu-id="0201c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0201c-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="0201c-109">Pobiera określony dokument polecenia Uruchom dla elementu "RunPowerShellScript" w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="0201c-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="0201c-110">Lokalizacja Get-AzVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="0201c-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="0201c-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0201c-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="0201c-112">Wyświetla wszystkie dostępne polecenia Uruchom w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="0201c-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="0201c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0201c-113">PARAMETERS</span></span>

### <span data-ttu-id="0201c-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="0201c-114">-CommandId</span></span>
<span data-ttu-id="0201c-115">Identyfikator polecenia.</span><span class="sxs-lookup"><span data-stu-id="0201c-115">The command id.</span></span>

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

### <span data-ttu-id="0201c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0201c-116">-DefaultProfile</span></span>
<span data-ttu-id="0201c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0201c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0201c-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0201c-118">-Location</span></span>
<span data-ttu-id="0201c-119">Lokalizacja, w której są wysyłane zapytania dotyczące polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="0201c-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="0201c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0201c-120">CommonParameters</span></span>
<span data-ttu-id="0201c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0201c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0201c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0201c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0201c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0201c-123">INPUTS</span></span>

### <span data-ttu-id="0201c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0201c-124">System.String</span></span>

## <span data-ttu-id="0201c-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0201c-125">OUTPUTS</span></span>

### <span data-ttu-id="0201c-126">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="0201c-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="0201c-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0201c-127">NOTES</span></span>

## <span data-ttu-id="0201c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0201c-128">RELATED LINKS</span></span>

