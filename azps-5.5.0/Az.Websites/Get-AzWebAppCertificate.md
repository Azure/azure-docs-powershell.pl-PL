---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241571"
---
# <span data-ttu-id="d2156-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d2156-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="d2156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2156-102">SYNOPSIS</span></span>
<span data-ttu-id="d2156-103">Otrzymuje certyfikat aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d2156-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="d2156-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2156-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2156-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2156-105">DESCRIPTION</span></span>
<span data-ttu-id="d2156-106">Polecenie **cmdlet Get-AzWebAppCertificate** pobiera informacje o certyfikatach aplikacji Azure Web App skojarzonych z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2156-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="d2156-107">Jeśli znasz certyfikat thumbprint, możesz również użyć tego polecenia cmdlet w celu uzyskania informacji o określonym certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="d2156-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="d2156-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2156-108">EXAMPLES</span></span>

### <span data-ttu-id="d2156-109">Przykład 1. Uzyskiwanie certyfikatów aplikacji Web App w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d2156-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="d2156-110">To polecenie zwraca informacje o przekazanych certyfikatach aplikacji Web App skojarzonych z grupą zasobów ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d2156-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="d2156-111">Przykład 2. Uzyskiwanie określonego certyfikatu aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="d2156-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="d2156-112">To polecenie pobiera certyfikat aplikacji ContosoResourceGroup Web App z kciukiem E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="d2156-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="d2156-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2156-113">PARAMETERS</span></span>

### <span data-ttu-id="d2156-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2156-114">-DefaultProfile</span></span>
<span data-ttu-id="d2156-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2156-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2156-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2156-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2156-117">Określa nazwę grupy zasobów, do których jest przypisany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="d2156-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2156-118">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d2156-118">-Thumbprint</span></span>
<span data-ttu-id="d2156-119">Określa identyfikator unikatowy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d2156-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2156-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2156-120">CommonParameters</span></span>
<span data-ttu-id="d2156-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2156-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2156-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2156-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2156-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2156-123">INPUTS</span></span>

### <span data-ttu-id="d2156-124">Brak</span><span class="sxs-lookup"><span data-stu-id="d2156-124">None</span></span>

## <span data-ttu-id="d2156-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2156-125">OUTPUTS</span></span>

### <span data-ttu-id="d2156-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="d2156-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="d2156-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2156-127">NOTES</span></span>

## <span data-ttu-id="d2156-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2156-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2156-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="d2156-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


