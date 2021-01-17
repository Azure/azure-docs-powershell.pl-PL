---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323111"
---
# <span data-ttu-id="526cc-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="526cc-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="526cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="526cc-102">SYNOPSIS</span></span>
<span data-ttu-id="526cc-103">Pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="526cc-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="526cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="526cc-104">SYNTAX</span></span>

### <span data-ttu-id="526cc-105">S1</span><span class="sxs-lookup"><span data-stu-id="526cc-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="526cc-106">S2</span><span class="sxs-lookup"><span data-stu-id="526cc-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="526cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="526cc-107">DESCRIPTION</span></span>
<span data-ttu-id="526cc-108">Polecenie cmdlet **Get-AzWebAppPublishingProfile** pobiera profil publikowania aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="526cc-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="526cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="526cc-109">EXAMPLES</span></span>

### <span data-ttu-id="526cc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="526cc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="526cc-111">To polecenie pobiera profil publikowania w formacie FTP dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web-zachód i zapisuje je w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="526cc-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="526cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="526cc-112">PARAMETERS</span></span>

### <span data-ttu-id="526cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526cc-113">-DefaultProfile</span></span>
<span data-ttu-id="526cc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="526cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="526cc-115">-Format</span><span class="sxs-lookup"><span data-stu-id="526cc-115">-Format</span></span>
<span data-ttu-id="526cc-116">Formaty</span><span class="sxs-lookup"><span data-stu-id="526cc-116">Format</span></span>

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

### <span data-ttu-id="526cc-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="526cc-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="526cc-118">Dołączanie punktów końcowych odzyskiwania po awarii w przypadku wartości prawda</span><span class="sxs-lookup"><span data-stu-id="526cc-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526cc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="526cc-119">-Name</span></span>
<span data-ttu-id="526cc-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="526cc-120">WebApp Name</span></span>

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

### <span data-ttu-id="526cc-121">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="526cc-121">-OutputFile</span></span>
<span data-ttu-id="526cc-122">Plik wyjściowy</span><span class="sxs-lookup"><span data-stu-id="526cc-122">Output File</span></span>

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

### <span data-ttu-id="526cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="526cc-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="526cc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="526cc-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="526cc-125">-WebApp</span></span>
<span data-ttu-id="526cc-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="526cc-126">WebApp Object</span></span>

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

### <span data-ttu-id="526cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526cc-127">CommonParameters</span></span>
<span data-ttu-id="526cc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="526cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526cc-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526cc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526cc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="526cc-130">INPUTS</span></span>

### <span data-ttu-id="526cc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="526cc-131">System.String</span></span>

### <span data-ttu-id="526cc-132">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="526cc-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="526cc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="526cc-133">OUTPUTS</span></span>

### <span data-ttu-id="526cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="526cc-134">System.String</span></span>

## <span data-ttu-id="526cc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="526cc-135">NOTES</span></span>

## <span data-ttu-id="526cc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="526cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="526cc-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="526cc-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="526cc-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="526cc-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


