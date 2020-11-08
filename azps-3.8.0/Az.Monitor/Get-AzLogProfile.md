---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053478"
---
# <span data-ttu-id="f9aeb-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f9aeb-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="f9aeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="f9aeb-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="f9aeb-103">Gets a log profile.</span></span>

## <span data-ttu-id="f9aeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9aeb-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9aeb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9aeb-105">DESCRIPTION</span></span>
<span data-ttu-id="f9aeb-106">Polecenie cmdlet **Get-AzLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="f9aeb-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="f9aeb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9aeb-107">EXAMPLES</span></span>

## <span data-ttu-id="f9aeb-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9aeb-108">PARAMETERS</span></span>

### <span data-ttu-id="f9aeb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9aeb-109">-DefaultProfile</span></span>
<span data-ttu-id="f9aeb-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f9aeb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9aeb-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9aeb-111">-Name</span></span>
<span data-ttu-id="f9aeb-112">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="f9aeb-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="f9aeb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9aeb-113">CommonParameters</span></span>
<span data-ttu-id="f9aeb-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9aeb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9aeb-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9aeb-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9aeb-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9aeb-116">INPUTS</span></span>

### <span data-ttu-id="f9aeb-117">System. String</span><span class="sxs-lookup"><span data-stu-id="f9aeb-117">System.String</span></span>

## <span data-ttu-id="f9aeb-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9aeb-118">OUTPUTS</span></span>

### <span data-ttu-id="f9aeb-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="f9aeb-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="f9aeb-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9aeb-120">NOTES</span></span>

## <span data-ttu-id="f9aeb-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9aeb-121">RELATED LINKS</span></span>

[<span data-ttu-id="f9aeb-122">Dodaj-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f9aeb-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="f9aeb-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f9aeb-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


