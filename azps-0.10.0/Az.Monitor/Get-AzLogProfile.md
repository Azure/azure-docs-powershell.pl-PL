---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 5d99bafdd011409eae322c60db6e596d3c77cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891190"
---
# <span data-ttu-id="a4144-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4144-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="a4144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4144-102">SYNOPSIS</span></span>
<span data-ttu-id="a4144-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="a4144-103">Gets a log profile.</span></span>

## <span data-ttu-id="a4144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4144-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4144-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4144-105">DESCRIPTION</span></span>
<span data-ttu-id="a4144-106">Polecenie cmdlet **Get-AzLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="a4144-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="a4144-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4144-107">EXAMPLES</span></span>

## <span data-ttu-id="a4144-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4144-108">PARAMETERS</span></span>

### <span data-ttu-id="a4144-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4144-109">-DefaultProfile</span></span>
<span data-ttu-id="a4144-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4144-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4144-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4144-111">-Name</span></span>
<span data-ttu-id="a4144-112">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="a4144-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="a4144-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4144-113">CommonParameters</span></span>
<span data-ttu-id="a4144-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4144-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4144-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4144-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4144-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4144-116">INPUTS</span></span>

### <span data-ttu-id="a4144-117">System. String</span><span class="sxs-lookup"><span data-stu-id="a4144-117">System.String</span></span>

## <span data-ttu-id="a4144-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4144-118">OUTPUTS</span></span>

### <span data-ttu-id="a4144-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="a4144-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="a4144-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4144-120">NOTES</span></span>

## <span data-ttu-id="a4144-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4144-121">RELATED LINKS</span></span>

[<span data-ttu-id="a4144-122">Dodaj-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4144-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="a4144-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a4144-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


