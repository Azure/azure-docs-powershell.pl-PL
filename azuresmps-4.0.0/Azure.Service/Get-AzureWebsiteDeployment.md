---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055475"
---
# <span data-ttu-id="97e1d-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="97e1d-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="97e1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="97e1d-103">Pobiera wdrożenia witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="97e1d-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="97e1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97e1d-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97e1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97e1d-105">DESCRIPTION</span></span>
<span data-ttu-id="97e1d-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97e1d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="97e1d-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="97e1d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="97e1d-108">Pobiera wdrożenia witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="97e1d-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="97e1d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97e1d-109">EXAMPLES</span></span>

## <span data-ttu-id="97e1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97e1d-110">PARAMETERS</span></span>

### <span data-ttu-id="97e1d-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="97e1d-111">-CommitId</span></span>
<span data-ttu-id="97e1d-112">Określa unikatowy identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="97e1d-112">Specifies the unique ID for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-113">-Szczegóły</span><span class="sxs-lookup"><span data-stu-id="97e1d-113">-Details</span></span>
<span data-ttu-id="97e1d-114">Przedstawia szczegółowe informacje na temat wdrożeń.</span><span class="sxs-lookup"><span data-stu-id="97e1d-114">Shows detailed information about the deployments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="97e1d-115">-MaxResults</span></span>
<span data-ttu-id="97e1d-116">Określa największą liczbę wyników, które ma zwrócić polecenie.</span><span class="sxs-lookup"><span data-stu-id="97e1d-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97e1d-117">-Name</span></span>
<span data-ttu-id="97e1d-118">Określa nazwę witryny sieci Web, dla której mają zostać wyświetlone informacje dotyczące wdrażania.</span><span class="sxs-lookup"><span data-stu-id="97e1d-118">Specifies the name of the website for which you want to get deployment information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="97e1d-119">-Profile</span></span>
<span data-ttu-id="97e1d-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e1d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97e1d-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="97e1d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="97e1d-122">-Slot</span></span>
<span data-ttu-id="97e1d-123">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="97e1d-123">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e1d-124">CommonParameters</span></span>
<span data-ttu-id="97e1d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e1d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e1d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e1d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97e1d-127">INPUTS</span></span>

## <span data-ttu-id="97e1d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97e1d-128">OUTPUTS</span></span>

## <span data-ttu-id="97e1d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97e1d-129">NOTES</span></span>

## <span data-ttu-id="97e1d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97e1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="97e1d-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="97e1d-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


