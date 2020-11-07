---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719665"
---
# <span data-ttu-id="6fcab-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6fcab-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="6fcab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fcab-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcab-103">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="6fcab-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fcab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fcab-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fcab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fcab-105">DESCRIPTION</span></span>
<span data-ttu-id="6fcab-106">Pobierz dokument polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="6fcab-106">Get run command document.</span></span>

## <span data-ttu-id="6fcab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fcab-107">EXAMPLES</span></span>

### <span data-ttu-id="6fcab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fcab-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="6fcab-109">Pobiera określony dokument polecenia Uruchom dla elementu "RunPowerShellScript" w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="6fcab-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="6fcab-110">Lokalizacja Get-AzureRmVMRunCommandDocument $loc</span><span class="sxs-lookup"><span data-stu-id="6fcab-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="6fcab-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6fcab-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="6fcab-112">Wyświetla wszystkie dostępne polecenia Uruchom w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="6fcab-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="6fcab-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fcab-113">PARAMETERS</span></span>

### <span data-ttu-id="6fcab-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="6fcab-114">-CommandId</span></span>
<span data-ttu-id="6fcab-115">Identyfikator polecenia.</span><span class="sxs-lookup"><span data-stu-id="6fcab-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fcab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcab-116">-DefaultProfile</span></span>
<span data-ttu-id="6fcab-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fcab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fcab-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6fcab-118">-Location</span></span>
<span data-ttu-id="6fcab-119">Lokalizacja, w której są wysyłane zapytania dotyczące polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="6fcab-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="6fcab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcab-120">CommonParameters</span></span>
<span data-ttu-id="6fcab-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fcab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcab-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcab-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fcab-123">INPUTS</span></span>

### <span data-ttu-id="6fcab-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6fcab-124">System.String</span></span>

## <span data-ttu-id="6fcab-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fcab-125">OUTPUTS</span></span>

### <span data-ttu-id="6fcab-126">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6fcab-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="6fcab-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fcab-127">NOTES</span></span>

## <span data-ttu-id="6fcab-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fcab-128">RELATED LINKS</span></span>

