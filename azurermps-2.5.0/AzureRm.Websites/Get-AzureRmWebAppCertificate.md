---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
ms.openlocfilehash: dcdba23de872ed0f1518188387c6f7e2d357c909
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897766"
---
# <span data-ttu-id="40962-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="40962-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="40962-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40962-102">SYNOPSIS</span></span>
<span data-ttu-id="40962-103">Pobiera certyfikat aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="40962-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40962-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40962-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40962-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40962-105">DESCRIPTION</span></span>
<span data-ttu-id="40962-106">Polecenie cmdlet **Get-AzureRmWebAppCertificate** pobiera informacje o certyfikatach aplikacji Azure Web App skojarzonych z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="40962-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="40962-107">Jeśli znasz odcisk palca certyfikatu, możesz również użyć tego polecenia cmdlet, aby uzyskać informacje o określonym certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="40962-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="40962-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40962-108">EXAMPLES</span></span>

### <span data-ttu-id="40962-109">Przykład 1: uzyskiwanie certyfikatów aplikacji sieci Web w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="40962-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="40962-110">To polecenie zwraca informacje o przekazanych certyfikatach aplikacji sieci Web skojarzonych z grupą ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40962-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="40962-111">Przykład 2: uzyskiwanie określonego certyfikatu aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="40962-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="40962-112">To polecenie pobiera certyfikat aplikacji ContosoResourceGroup Web App z E3A38EBA60CAA1C162785A2E1C44A15AD450199C3em odcisku palca.</span><span class="sxs-lookup"><span data-stu-id="40962-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="40962-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40962-113">PARAMETERS</span></span>

### <span data-ttu-id="40962-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40962-114">-DefaultProfile</span></span>
<span data-ttu-id="40962-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40962-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40962-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40962-116">-ResourceGroupName</span></span>
<span data-ttu-id="40962-117">Określa nazwę grupy zasobów, do której przypisano certyfikat.</span><span class="sxs-lookup"><span data-stu-id="40962-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40962-118">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="40962-118">-Thumbprint</span></span>
<span data-ttu-id="40962-119">Określa unikatowy identyfikator certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="40962-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40962-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40962-120">CommonParameters</span></span>
<span data-ttu-id="40962-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40962-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40962-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40962-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40962-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40962-123">INPUTS</span></span>

### <span data-ttu-id="40962-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="40962-124">None</span></span>
<span data-ttu-id="40962-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="40962-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40962-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40962-126">OUTPUTS</span></span>

## <span data-ttu-id="40962-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40962-127">NOTES</span></span>

## <span data-ttu-id="40962-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40962-128">RELATED LINKS</span></span>

[<span data-ttu-id="40962-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="40962-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


