---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504107"
---
# <span data-ttu-id="d7f01-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="d7f01-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="d7f01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7f01-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f01-103">Pobieranie dokumentu polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="d7f01-103">Get a run command document.</span></span>

## <span data-ttu-id="d7f01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7f01-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f01-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7f01-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f01-106">Pobieranie dokumentu polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="d7f01-106">Get a run command document.</span></span>

## <span data-ttu-id="d7f01-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7f01-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f01-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7f01-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="d7f01-109">Pobiera określony dokument polecenia Uruchom dla elementu "RunPowerShellScript" w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="d7f01-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="d7f01-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d7f01-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="d7f01-111">Wyświetla wszystkie dostępne polecenia Uruchom w obszarze "zachód".</span><span class="sxs-lookup"><span data-stu-id="d7f01-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="d7f01-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7f01-112">PARAMETERS</span></span>

### <span data-ttu-id="d7f01-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="d7f01-113">-CommandId</span></span>
<span data-ttu-id="d7f01-114">Identyfikator polecenia.</span><span class="sxs-lookup"><span data-stu-id="d7f01-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f01-115">-DefaultProfile</span></span>
<span data-ttu-id="d7f01-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f01-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7f01-117">-Location</span></span>
<span data-ttu-id="d7f01-118">Lokalizacja, w której są badane polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="d7f01-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="d7f01-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f01-119">CommonParameters</span></span>
<span data-ttu-id="d7f01-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f01-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f01-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7f01-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f01-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7f01-122">INPUTS</span></span>

### <span data-ttu-id="d7f01-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d7f01-123">System.String</span></span>

## <span data-ttu-id="d7f01-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7f01-124">OUTPUTS</span></span>

### <span data-ttu-id="d7f01-125">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="d7f01-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="d7f01-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7f01-126">NOTES</span></span>

## <span data-ttu-id="d7f01-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7f01-127">RELATED LINKS</span></span>
