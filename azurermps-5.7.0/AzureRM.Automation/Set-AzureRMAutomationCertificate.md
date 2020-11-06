---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550712"
---
# <span data-ttu-id="5d685-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d685-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="5d685-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d685-102">SYNOPSIS</span></span>
<span data-ttu-id="5d685-103">Modyfikuje konfigurację certyfikatu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5d685-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d685-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d685-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d685-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d685-105">DESCRIPTION</span></span>
<span data-ttu-id="5d685-106">Polecenie cmdlet **Set-AzureRmAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5d685-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="5d685-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d685-107">EXAMPLES</span></span>

### <span data-ttu-id="5d685-108">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5d685-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5d685-109">Pierwsze polecenie konwertuje hasło zwykłego tekstu na ciąg bezpieczny za pomocą polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="5d685-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="5d685-110">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="5d685-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="5d685-111">Drugie polecenie modyfikuje certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="5d685-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="5d685-112">W poleceniu użyto hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="5d685-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="5d685-113">Polecenie określa nazwę konta i ścieżkę pliku, który jest wysyłany.</span><span class="sxs-lookup"><span data-stu-id="5d685-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="5d685-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d685-114">PARAMETERS</span></span>

### <span data-ttu-id="5d685-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d685-115">-AutomationAccountName</span></span>
<span data-ttu-id="5d685-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="5d685-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="5d685-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d685-117">-DefaultProfile</span></span>
<span data-ttu-id="5d685-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d685-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d685-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="5d685-119">-Description</span></span>
<span data-ttu-id="5d685-120">Określa opis certyfikatu modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d685-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5d685-121">— Możliwy do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="5d685-121">-Exportable</span></span>
<span data-ttu-id="5d685-122">Określa, czy można eksportować certyfikat.</span><span class="sxs-lookup"><span data-stu-id="5d685-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d685-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d685-123">-Name</span></span>
<span data-ttu-id="5d685-124">Określa nazwę certyfikatu modyfikowanego przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="5d685-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5d685-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="5d685-125">-Password</span></span>
<span data-ttu-id="5d685-126">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5d685-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="5d685-127">-Path</span><span class="sxs-lookup"><span data-stu-id="5d685-127">-Path</span></span>
<span data-ttu-id="5d685-128">Określa ścieżkę do pliku skryptu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="5d685-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="5d685-129">Plik może być plikiem cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="5d685-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="5d685-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d685-130">-ResourceGroupName</span></span>
<span data-ttu-id="5d685-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="5d685-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="5d685-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d685-132">CommonParameters</span></span>
<span data-ttu-id="5d685-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d685-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d685-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d685-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d685-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d685-135">INPUTS</span></span>

### <span data-ttu-id="5d685-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5d685-136">None</span></span>
<span data-ttu-id="5d685-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5d685-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d685-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d685-138">OUTPUTS</span></span>

### <span data-ttu-id="5d685-139">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="5d685-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="5d685-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d685-140">NOTES</span></span>

## <span data-ttu-id="5d685-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d685-141">RELATED LINKS</span></span>

[<span data-ttu-id="5d685-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d685-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="5d685-143">Nowe — AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d685-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="5d685-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d685-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


