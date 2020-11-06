---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543299"
---
# <span data-ttu-id="80bcc-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="80bcc-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="80bcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="80bcc-103">Pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="80bcc-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80bcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80bcc-104">SYNTAX</span></span>

### <span data-ttu-id="80bcc-105">S1</span><span class="sxs-lookup"><span data-stu-id="80bcc-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80bcc-106">S2</span><span class="sxs-lookup"><span data-stu-id="80bcc-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80bcc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="80bcc-108">Polecenie cmdlet **Get-AzureRmWebAppPublishingProfile** pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="80bcc-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="80bcc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80bcc-109">EXAMPLES</span></span>

### <span data-ttu-id="80bcc-110">1:1</span><span class="sxs-lookup"><span data-stu-id="80bcc-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="80bcc-111">To polecenie pobiera profil publikowania w formacie FTP dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="80bcc-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="80bcc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80bcc-112">PARAMETERS</span></span>

### <span data-ttu-id="80bcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bcc-113">-DefaultProfile</span></span>
<span data-ttu-id="80bcc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80bcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80bcc-115">-Format</span><span class="sxs-lookup"><span data-stu-id="80bcc-115">-Format</span></span>
<span data-ttu-id="80bcc-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="80bcc-116">Format</span></span>

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

### <span data-ttu-id="80bcc-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="80bcc-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="80bcc-118">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="80bcc-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bcc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80bcc-119">-Name</span></span>
<span data-ttu-id="80bcc-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="80bcc-120">WebApp Name</span></span>

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

### <span data-ttu-id="80bcc-121">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="80bcc-121">-OutputFile</span></span>
<span data-ttu-id="80bcc-122">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="80bcc-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="80bcc-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="80bcc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="80bcc-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="80bcc-125">-WebApp</span></span>
<span data-ttu-id="80bcc-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="80bcc-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80bcc-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="80bcc-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="80bcc-128">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="80bcc-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bcc-129">CommonParameters</span></span>
<span data-ttu-id="80bcc-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80bcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bcc-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80bcc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bcc-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80bcc-132">INPUTS</span></span>

### <span data-ttu-id="80bcc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="80bcc-133">System.String</span></span>

### <span data-ttu-id="80bcc-134">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="80bcc-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="80bcc-135">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80bcc-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="80bcc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80bcc-136">OUTPUTS</span></span>

### <span data-ttu-id="80bcc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="80bcc-137">System.String</span></span>

## <span data-ttu-id="80bcc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80bcc-138">NOTES</span></span>

## <span data-ttu-id="80bcc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80bcc-139">RELATED LINKS</span></span>

[<span data-ttu-id="80bcc-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="80bcc-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="80bcc-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80bcc-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


