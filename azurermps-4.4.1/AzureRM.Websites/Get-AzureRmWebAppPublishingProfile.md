---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542779"
---
# <span data-ttu-id="36174-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="36174-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="36174-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36174-102">SYNOPSIS</span></span>
<span data-ttu-id="36174-103">Pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="36174-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36174-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36174-104">SYNTAX</span></span>

### <span data-ttu-id="36174-105">S1</span><span class="sxs-lookup"><span data-stu-id="36174-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36174-106">S2</span><span class="sxs-lookup"><span data-stu-id="36174-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36174-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36174-107">DESCRIPTION</span></span>
<span data-ttu-id="36174-108">Polecenie cmdlet **Get-AzureRmWebAppPublishingProfile** pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="36174-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="36174-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36174-109">EXAMPLES</span></span>

### <span data-ttu-id="36174-110">1:1</span><span class="sxs-lookup"><span data-stu-id="36174-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="36174-111">To polecenie pobiera profil publikowania w formacie FTP dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="36174-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="36174-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36174-112">PARAMETERS</span></span>

### <span data-ttu-id="36174-113">-Format</span><span class="sxs-lookup"><span data-stu-id="36174-113">-Format</span></span>
<span data-ttu-id="36174-114">Formaty</span><span class="sxs-lookup"><span data-stu-id="36174-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36174-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36174-115">-Name</span></span>
<span data-ttu-id="36174-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="36174-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36174-117">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="36174-117">-OutputFile</span></span>
<span data-ttu-id="36174-118">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="36174-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36174-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36174-119">-ResourceGroupName</span></span>
<span data-ttu-id="36174-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="36174-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36174-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="36174-121">-WebApp</span></span>
<span data-ttu-id="36174-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="36174-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36174-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36174-123">-DefaultProfile</span></span>
<span data-ttu-id="36174-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36174-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36174-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36174-125">CommonParameters</span></span>
<span data-ttu-id="36174-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36174-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36174-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36174-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36174-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36174-128">INPUTS</span></span>

### <span data-ttu-id="36174-129">Klienta</span><span class="sxs-lookup"><span data-stu-id="36174-129">Site</span></span>
<span data-ttu-id="36174-130">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="36174-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="36174-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36174-131">OUTPUTS</span></span>

## <span data-ttu-id="36174-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36174-132">NOTES</span></span>

## <span data-ttu-id="36174-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36174-133">RELATED LINKS</span></span>

[<span data-ttu-id="36174-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="36174-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="36174-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="36174-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


