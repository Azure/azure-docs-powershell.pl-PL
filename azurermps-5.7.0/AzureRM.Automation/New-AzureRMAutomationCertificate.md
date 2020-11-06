---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525365"
---
# <span data-ttu-id="0e8d2-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8d2-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="0e8d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8d2-103">Tworzy certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e8d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e8d2-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e8d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8d2-106">Polecenie cmdlet **New-AzureRmAutomationCertificate** tworzy certyfikat w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="0e8d2-107">Podaj ścieżkę do pliku certyfikatu, który chcesz przekazać.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="0e8d2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e8d2-108">EXAMPLES</span></span>

### <span data-ttu-id="0e8d2-109">Przykład 1. Tworzenie nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="0e8d2-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0e8d2-110">Pierwsze polecenie konwertuje hasło zwykłego tekstu na ciąg bezpieczny za pomocą polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0e8d2-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="0e8d2-112">Drugie polecenie tworzy certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="0e8d2-113">W poleceniu użyto hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="0e8d2-114">Polecenie określa nazwę konta i ścieżkę pliku, który jest wysyłany.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="0e8d2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e8d2-115">PARAMETERS</span></span>

### <span data-ttu-id="0e8d2-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e8d2-116">-AutomationAccountName</span></span>
<span data-ttu-id="0e8d2-117">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet przechowuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8d2-118">-DefaultProfile</span></span>
<span data-ttu-id="0e8d2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e8d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8d2-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="0e8d2-120">-Description</span></span>
<span data-ttu-id="0e8d2-121">Określa opis certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="0e8d2-122">— Możliwy do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="0e8d2-122">-Exportable</span></span>
<span data-ttu-id="0e8d2-123">Określa, czy można eksportować certyfikat.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e8d2-124">-Name</span></span>
<span data-ttu-id="0e8d2-125">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-125">Specifies the name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="0e8d2-126">-Password</span></span>
<span data-ttu-id="0e8d2-127">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-128">-Path</span><span class="sxs-lookup"><span data-stu-id="0e8d2-128">-Path</span></span>
<span data-ttu-id="0e8d2-129">Określa ścieżkę do pliku skryptu, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="0e8d2-130">Plik może być plikiem cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e8d2-132">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8d2-133">CommonParameters</span></span>
<span data-ttu-id="0e8d2-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8d2-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8d2-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e8d2-136">INPUTS</span></span>

### <span data-ttu-id="0e8d2-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e8d2-137">None</span></span>
<span data-ttu-id="0e8d2-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0e8d2-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e8d2-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e8d2-139">OUTPUTS</span></span>

### <span data-ttu-id="0e8d2-140">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0e8d2-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0e8d2-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e8d2-141">NOTES</span></span>

## <span data-ttu-id="0e8d2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e8d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e8d2-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8d2-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0e8d2-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8d2-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0e8d2-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8d2-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


