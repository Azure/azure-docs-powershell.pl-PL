---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891950"
---
# <span data-ttu-id="86eab-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-101">Get-AzWebApp</span></span>

## <span data-ttu-id="86eab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86eab-102">SYNOPSIS</span></span>
<span data-ttu-id="86eab-103">Pobiera aplikacje sieci Web platformy Azure w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="86eab-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="86eab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86eab-104">SYNTAX</span></span>

### <span data-ttu-id="86eab-105">S1</span><span class="sxs-lookup"><span data-stu-id="86eab-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86eab-106">S2</span><span class="sxs-lookup"><span data-stu-id="86eab-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86eab-107">S3</span><span class="sxs-lookup"><span data-stu-id="86eab-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86eab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="86eab-108">DESCRIPTION</span></span>
<span data-ttu-id="86eab-109">Polecenie cmdlet **Get-AzWebApp** pobiera informacje o aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="86eab-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="86eab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86eab-110">EXAMPLES</span></span>

### <span data-ttu-id="86eab-111">Przykład 1: uzyskiwanie aplikacji sieci Web z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="86eab-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="86eab-112">To polecenie umożliwia wyświetlenie aplikacji sieci Web o nazwie ContosoSite należącej do obszaru domyślnego Grupa zasobów — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="86eab-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="86eab-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86eab-113">PARAMETERS</span></span>

### <span data-ttu-id="86eab-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="86eab-114">-AppServicePlan</span></span>
<span data-ttu-id="86eab-115">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="86eab-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86eab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86eab-116">-DefaultProfile</span></span>
<span data-ttu-id="86eab-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86eab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86eab-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86eab-118">-Location</span></span>
<span data-ttu-id="86eab-119">Pozycję</span><span class="sxs-lookup"><span data-stu-id="86eab-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86eab-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86eab-120">-Name</span></span>
<span data-ttu-id="86eab-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="86eab-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86eab-122">-ResourceGroupName</span></span>
<span data-ttu-id="86eab-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="86eab-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86eab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86eab-124">CommonParameters</span></span>
<span data-ttu-id="86eab-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86eab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86eab-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86eab-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86eab-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86eab-127">INPUTS</span></span>

### <span data-ttu-id="86eab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="86eab-128">System.String</span></span>

## <span data-ttu-id="86eab-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86eab-129">OUTPUTS</span></span>

### <span data-ttu-id="86eab-130">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="86eab-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="86eab-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86eab-131">NOTES</span></span>

## <span data-ttu-id="86eab-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86eab-132">RELATED LINKS</span></span>

[<span data-ttu-id="86eab-133">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="86eab-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="86eab-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="86eab-136">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="86eab-137">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="86eab-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


