---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897758"
---
# <span data-ttu-id="7e5d6-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7e5d6-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="7e5d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5d6-103">Pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e5d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e5d6-104">SYNTAX</span></span>

### <span data-ttu-id="7e5d6-105">S1</span><span class="sxs-lookup"><span data-stu-id="7e5d6-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e5d6-106">S2</span><span class="sxs-lookup"><span data-stu-id="7e5d6-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e5d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e5d6-107">DESCRIPTION</span></span>
<span data-ttu-id="7e5d6-108">Polecenie cmdlet **Get-AzureRmWebAppPublishingProfile** pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="7e5d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e5d6-109">EXAMPLES</span></span>

### <span data-ttu-id="7e5d6-110">1:1</span><span class="sxs-lookup"><span data-stu-id="7e5d6-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="7e5d6-111">To polecenie pobiera profil publikowania w formacie FTP dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="7e5d6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e5d6-112">PARAMETERS</span></span>

### <span data-ttu-id="7e5d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5d6-113">-DefaultProfile</span></span>
<span data-ttu-id="7e5d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e5d6-115">-Format</span><span class="sxs-lookup"><span data-stu-id="7e5d6-115">-Format</span></span>
<span data-ttu-id="7e5d6-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="7e5d6-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5d6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e5d6-117">-Name</span></span>
<span data-ttu-id="7e5d6-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e5d6-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5d6-119">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="7e5d6-119">-OutputFile</span></span>
<span data-ttu-id="7e5d6-120">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="7e5d6-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e5d6-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7e5d6-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5d6-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e5d6-123">-WebApp</span></span>
<span data-ttu-id="7e5d6-124">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e5d6-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5d6-125">CommonParameters</span></span>
<span data-ttu-id="7e5d6-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5d6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e5d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5d6-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e5d6-128">INPUTS</span></span>

### <span data-ttu-id="7e5d6-129">Klienta</span><span class="sxs-lookup"><span data-stu-id="7e5d6-129">Site</span></span>
<span data-ttu-id="7e5d6-130">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7e5d6-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7e5d6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e5d6-131">OUTPUTS</span></span>

## <span data-ttu-id="7e5d6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e5d6-132">NOTES</span></span>

## <span data-ttu-id="7e5d6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e5d6-133">RELATED LINKS</span></span>

[<span data-ttu-id="7e5d6-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7e5d6-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="7e5d6-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e5d6-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


