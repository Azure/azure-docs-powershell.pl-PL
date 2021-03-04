---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981722"
---
# <span data-ttu-id="2b64e-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="2b64e-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="2b64e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b64e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b64e-103">Usuwa certyfikat zarządzany przez usługę aplikacji dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2b64e-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="2b64e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b64e-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b64e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b64e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b64e-106">Polecenie **cmdlet Remove-AzWebAppCertificate** usuwa certyfikat zarządzany przez usługę aplikacji Azure</span><span class="sxs-lookup"><span data-stu-id="2b64e-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="2b64e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b64e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b64e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b64e-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="2b64e-109">To polecenie usuwa certyfikat zarządzany przez usługę aplikacji dla danej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2b64e-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="2b64e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b64e-110">PARAMETERS</span></span>

### <span data-ttu-id="2b64e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b64e-111">-DefaultProfile</span></span>
<span data-ttu-id="2b64e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b64e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b64e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b64e-113">-ResourceGroupName</span></span>
<span data-ttu-id="2b64e-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b64e-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b64e-115">- ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="2b64e-115">-ThumbPrint</span></span>
<span data-ttu-id="2b64e-116">Thumbprint of the certificate that already exists in web space.</span><span class="sxs-lookup"><span data-stu-id="2b64e-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="2b64e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b64e-117">CommonParameters</span></span>
<span data-ttu-id="2b64e-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b64e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b64e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b64e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b64e-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b64e-120">INPUTS</span></span>

### <span data-ttu-id="2b64e-121">Brak</span><span class="sxs-lookup"><span data-stu-id="2b64e-121">None</span></span>

## <span data-ttu-id="2b64e-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b64e-122">OUTPUTS</span></span>

### <span data-ttu-id="2b64e-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="2b64e-123">System.Void</span></span>

## <span data-ttu-id="2b64e-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b64e-124">NOTES</span></span>

## <span data-ttu-id="2b64e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b64e-125">RELATED LINKS</span></span>
[<span data-ttu-id="2b64e-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="2b64e-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
