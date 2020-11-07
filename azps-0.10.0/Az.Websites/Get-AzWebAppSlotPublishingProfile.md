---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891910"
---
# <span data-ttu-id="a9bd9-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a9bd9-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a9bd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bd9-103">Pobiera profil publikowania miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a9bd9-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="a9bd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9bd9-104">SYNTAX</span></span>

### <span data-ttu-id="a9bd9-105">S1</span><span class="sxs-lookup"><span data-stu-id="a9bd9-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9bd9-106">S2</span><span class="sxs-lookup"><span data-stu-id="a9bd9-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9bd9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a9bd9-107">DESCRIPTION</span></span>
<span data-ttu-id="a9bd9-108">Polecenie cmdlet **Get-AzWebAppSlotPublishingProfile** pobiera profil publikowania aplikacji sieci Web dla określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="a9bd9-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="a9bd9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9bd9-109">EXAMPLES</span></span>

### <span data-ttu-id="a9bd9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9bd9-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="a9bd9-111">To polecenie pobiera profil publikowania w formacie FTP dla gniazd Slot001 odnoszących się do aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="a9bd9-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="a9bd9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9bd9-112">PARAMETERS</span></span>

### <span data-ttu-id="a9bd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bd9-113">-DefaultProfile</span></span>
<span data-ttu-id="a9bd9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9bd9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd9-115">-Format</span><span class="sxs-lookup"><span data-stu-id="a9bd9-115">-Format</span></span>
<span data-ttu-id="a9bd9-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="a9bd9-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9bd9-117">-Name</span></span>
<span data-ttu-id="a9bd9-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9bd9-118">WebApp Name</span></span>

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

### <span data-ttu-id="a9bd9-119">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="a9bd9-119">-OutputFile</span></span>
<span data-ttu-id="a9bd9-120">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="a9bd9-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9bd9-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9bd9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="a9bd9-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="a9bd9-123">-Slot</span></span>
<span data-ttu-id="a9bd9-124">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9bd9-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9bd9-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9bd9-125">-WebApp</span></span>
<span data-ttu-id="a9bd9-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="a9bd9-126">WebApp Object</span></span>

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

### <span data-ttu-id="a9bd9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bd9-127">CommonParameters</span></span>
<span data-ttu-id="a9bd9-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bd9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bd9-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9bd9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bd9-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9bd9-130">INPUTS</span></span>

### <span data-ttu-id="a9bd9-131">Klienta</span><span class="sxs-lookup"><span data-stu-id="a9bd9-131">Site</span></span>
<span data-ttu-id="a9bd9-132">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="a9bd9-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a9bd9-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9bd9-133">OUTPUTS</span></span>

## <span data-ttu-id="a9bd9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9bd9-134">NOTES</span></span>

## <span data-ttu-id="a9bd9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9bd9-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9bd9-136">Resetowanie — AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a9bd9-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="a9bd9-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9bd9-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a9bd9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a9bd9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
