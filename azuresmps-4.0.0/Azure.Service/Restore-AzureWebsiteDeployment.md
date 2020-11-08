---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054429"
---
# <span data-ttu-id="88c59-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="88c59-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="88c59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88c59-102">SYNOPSIS</span></span>
<span data-ttu-id="88c59-103">Ponowne wdrażanie wcześniejszego wdrożenia witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="88c59-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="88c59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88c59-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88c59-105">DESCRIPTION</span></span>
<span data-ttu-id="88c59-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="88c59-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="88c59-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="88c59-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="88c59-108">Polecenie cmdlet **Restore-AzureWebsiteDeployment** powoduje ponowne wdrożenie wcześniejszego wdrożenia witryny sieci Web na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="88c59-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="88c59-109">Ten proces zastępuje bieżące wdrożenie w ramach wybranego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="88c59-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="88c59-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88c59-110">EXAMPLES</span></span>

### <span data-ttu-id="88c59-111">Przykład 1: ponowne wdrażanie witryny</span><span class="sxs-lookup"><span data-stu-id="88c59-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="88c59-112">To polecenie powoduje ponowne wdrożenie wdrożenia o IDENTYFIKATORze f876543210 dla witryny internetowej o nazwie ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="88c59-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="88c59-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88c59-113">PARAMETERS</span></span>

### <span data-ttu-id="88c59-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="88c59-114">-CommitId</span></span>
<span data-ttu-id="88c59-115">Określa identyfikator wdrożenia do ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="88c59-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="88c59-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88c59-116">-Force</span></span>
<span data-ttu-id="88c59-117">Jeśli ta funkcja jest włączona, ponowne wdrożenie poprzedniego wdrożenia bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88c59-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="88c59-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88c59-118">-Name</span></span>
<span data-ttu-id="88c59-119">Określa nazwę witryny sieci Web do ponownego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="88c59-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="88c59-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="88c59-120">-Profile</span></span>
<span data-ttu-id="88c59-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c59-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88c59-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="88c59-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88c59-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="88c59-123">-Slot</span></span>
<span data-ttu-id="88c59-124">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="88c59-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="88c59-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88c59-125">-Confirm</span></span>
<span data-ttu-id="88c59-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c59-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c59-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c59-127">-WhatIf</span></span>
<span data-ttu-id="88c59-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c59-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c59-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88c59-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c59-130">CommonParameters</span></span>
<span data-ttu-id="88c59-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c59-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c59-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c59-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88c59-133">INPUTS</span></span>

## <span data-ttu-id="88c59-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88c59-134">OUTPUTS</span></span>

## <span data-ttu-id="88c59-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88c59-135">NOTES</span></span>

## <span data-ttu-id="88c59-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88c59-136">RELATED LINKS</span></span>

[<span data-ttu-id="88c59-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="88c59-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="88c59-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="88c59-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


