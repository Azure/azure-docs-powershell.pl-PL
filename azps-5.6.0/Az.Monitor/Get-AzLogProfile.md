---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980010"
---
# <span data-ttu-id="4ec40-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4ec40-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="4ec40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec40-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec40-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="4ec40-103">Gets a log profile.</span></span>

## <span data-ttu-id="4ec40-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ec40-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec40-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ec40-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec40-106">Polecenie **cmdlet Get-AzLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="4ec40-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="4ec40-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ec40-107">EXAMPLES</span></span>

## <span data-ttu-id="4ec40-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ec40-108">PARAMETERS</span></span>

### <span data-ttu-id="4ec40-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec40-109">-DefaultProfile</span></span>
<span data-ttu-id="4ec40-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4ec40-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ec40-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ec40-111">-Name</span></span>
<span data-ttu-id="4ec40-112">Określa nazwę profilu dziennika do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="4ec40-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="4ec40-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec40-113">CommonParameters</span></span>
<span data-ttu-id="4ec40-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec40-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec40-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ec40-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec40-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ec40-116">INPUTS</span></span>

### <span data-ttu-id="4ec40-117">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec40-117">System.String</span></span>

## <span data-ttu-id="4ec40-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ec40-118">OUTPUTS</span></span>

### <span data-ttu-id="4ec40-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="4ec40-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="4ec40-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ec40-120">NOTES</span></span>

## <span data-ttu-id="4ec40-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ec40-121">RELATED LINKS</span></span>

[<span data-ttu-id="4ec40-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4ec40-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="4ec40-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="4ec40-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


