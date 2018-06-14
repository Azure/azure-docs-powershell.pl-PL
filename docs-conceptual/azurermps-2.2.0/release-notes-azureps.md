---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854617"
---
# <a name="release-notes"></a><span data-ttu-id="da564-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="da564-103">Release notes</span></span>

<span data-ttu-id="da564-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="da564-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="da564-105">Wersja 2.2.0</span><span class="sxs-lookup"><span data-stu-id="da564-105">Version 2.2.0</span></span>
* <span data-ttu-id="da564-106">Compute</span><span class="sxs-lookup"><span data-stu-id="da564-106">Compute</span></span>
  - <span data-ttu-id="da564-107">Dodano obsługę pytania o stan szyfrowania z rozszerzenia AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="da564-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="da564-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="da564-108">DataFactory</span></span>
  - <span data-ttu-id="da564-109">Dodano nowe polecenie cmdlet do wyświetlania listy okien działania</span><span class="sxs-lookup"><span data-stu-id="da564-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="da564-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="da564-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="da564-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="da564-111">DataLake</span></span>
  - <span data-ttu-id="da564-112">Zmieniono parametr `Host` na `DatabaseHost` i dodano alias do `Host`</span><span class="sxs-lookup"><span data-stu-id="da564-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="da564-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="da564-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="da564-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="da564-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="da564-115">Dodano obsługę usuwania listy ACL i domyślnej listy ACL</span><span class="sxs-lookup"><span data-stu-id="da564-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="da564-116">Dodano obsługę pobierania i ustawiania nienazwanych uprawnień do plików i folderów</span><span class="sxs-lookup"><span data-stu-id="da564-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="da564-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="da564-117">KeyVault</span></span>
  - <span data-ttu-id="da564-118">Dodano obsługę certyfikatów</span><span class="sxs-lookup"><span data-stu-id="da564-118">Add support for certificates</span></span>
    + <span data-ttu-id="da564-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="da564-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="da564-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="da564-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="da564-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="da564-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="da564-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="da564-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="da564-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="da564-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="da564-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da564-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="da564-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da564-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="da564-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="da564-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="da564-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="da564-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="da564-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="da564-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="da564-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da564-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="da564-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="da564-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="da564-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="da564-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="da564-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="da564-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="da564-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da564-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="da564-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="da564-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="da564-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="da564-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="da564-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="da564-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="da564-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da564-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="da564-138">Sieć</span><span class="sxs-lookup"><span data-stu-id="da564-138">Network</span></span>

  - <span data-ttu-id="da564-139">Dodano nowy parametr przełącznika interfejsu sieciowego, aby włączyć/wyłączyć wydajniejsze sieci +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="da564-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="da564-140">Włączono polecenia cmdlet programu PowerShell funkcji bramy Active-Active</span><span class="sxs-lookup"><span data-stu-id="da564-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="da564-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="da564-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="da564-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="da564-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="da564-143">Dodano nowe polecenie cmdlet</span><span class="sxs-lookup"><span data-stu-id="da564-143">Added new cmdlet</span></span>
    + <span data-ttu-id="da564-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="da564-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="da564-145">Zasoby</span><span class="sxs-lookup"><span data-stu-id="da564-145">Resources</span></span>
  - <span data-ttu-id="da564-146">Obsługa stref w poleceniach cmdlet dostawcy i zasobów</span><span class="sxs-lookup"><span data-stu-id="da564-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="da564-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="da564-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="da564-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da564-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="da564-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da564-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="da564-150">Sql</span><span class="sxs-lookup"><span data-stu-id="da564-150">Sql</span></span>
  - <span data-ttu-id="da564-151">Dodano nowe polecenia cmdlet do zarządzania zasadami wykrywania zagrożeń usług Azure SQL na poziomie serwera</span><span class="sxs-lookup"><span data-stu-id="da564-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="da564-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da564-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="da564-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da564-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="da564-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da564-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="da564-155">Dodano nowe polecenia cmdlet do obsługi włączania/wyłączania zasad GeoBackupPolicy dla usług Azure SQL DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="da564-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="da564-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da564-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="da564-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da564-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="da564-158">Dodano nowe polecenia cmdlet dla interfejsów API usług Azure SQL Advisor i zalecanych akcji</span><span class="sxs-lookup"><span data-stu-id="da564-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="da564-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="da564-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="da564-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="da564-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="da564-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="da564-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="da564-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="da564-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="da564-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="da564-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="da564-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="da564-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="da564-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da564-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="da564-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da564-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="da564-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="da564-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="da564-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="da564-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="da564-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="da564-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="da564-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="da564-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
