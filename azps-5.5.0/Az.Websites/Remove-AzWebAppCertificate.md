---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182434"
---
# <span data-ttu-id="e7824-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="e7824-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="e7824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7824-102">SYNOPSIS</span></span>
<span data-ttu-id="e7824-103">Tworzy certyfikat zarządzany przez usługę aplikacji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e7824-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="e7824-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7824-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7824-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7824-105">DESCRIPTION</span></span>
<span data-ttu-id="e7824-106">Polecenie **cmdlet Remove-AzWebAppCertificate** tworzy certyfikat zarządzany usługi aplikacji Azure</span><span class="sxs-lookup"><span data-stu-id="e7824-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="e7824-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7824-107">EXAMPLES</span></span>

### <span data-ttu-id="e7824-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7824-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="e7824-109">To polecenie usuwa certyfikat zarządzany przez usługę aplikacji dla danej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e7824-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="e7824-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7824-110">PARAMETERS</span></span>

### <span data-ttu-id="e7824-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7824-111">-DefaultProfile</span></span>
<span data-ttu-id="e7824-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7824-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7824-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7824-113">-ResourceGroupName</span></span>
<span data-ttu-id="e7824-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7824-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7824-115">- ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="e7824-115">-ThumbPrint</span></span>
<span data-ttu-id="e7824-116">Thumbprint of the certificate that already exists in web space.</span><span class="sxs-lookup"><span data-stu-id="e7824-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7824-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7824-117">CommonParameters</span></span>
<span data-ttu-id="e7824-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7824-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7824-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7824-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7824-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7824-120">INPUTS</span></span>

### <span data-ttu-id="e7824-121">Brak</span><span class="sxs-lookup"><span data-stu-id="e7824-121">None</span></span>

## <span data-ttu-id="e7824-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7824-122">OUTPUTS</span></span>

### <span data-ttu-id="e7824-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="e7824-123">System.Void</span></span>

## <span data-ttu-id="e7824-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7824-124">NOTES</span></span>

## <span data-ttu-id="e7824-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7824-125">RELATED LINKS</span></span>
[<span data-ttu-id="e7824-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="e7824-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
